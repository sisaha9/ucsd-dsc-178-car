ARG BASE_IMAGE=sisaha9/jetson-ros
ARG ROS_DISTRO=galactic
ARG UBUNTU_CODENAME=focal

FROM ${BASE_IMAGE}:${ROS_DISTRO}
LABEL maintainer="Siddharth Saha <omadityasiddharth123@gmail.com>"

# Ensure we have the latest certificates installed before calling apt-get
RUN apt update ; apt-get install ca-certificates
RUN python3 -m pip install --upgrade pip
# Add apt-add-repository command.
RUN apt update && \
    apt install -y \
        software-properties-common && \
    rm -rf /var/lib/apt/lists/*

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key F6E65AC044F831AC80A06380C8B3A55A6F3EFCDE || apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-key F6E65AC044F831AC80A06380C8B3A55A6F3EFCDE
RUN add-apt-repository "deb https://librealsense.intel.com/Debian/apt-repo $(lsb_release -cs) main" -u
RUN apt update && \
    apt install -y \
        librealsense2-utils \
        librealsense2-dev
