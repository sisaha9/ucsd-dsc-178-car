ARG BASE_IMAGE=nvcr.io/nvidia/l4t-jetpack:r35.1.0
ARG ROS_DISTRO=galactic
ARG UBUNTU_CODENAME=focal

FROM ${BASE_IMAGE}
LABEL maintainer="Siddharth Saha <sisahawork@gmail.com>"

# Ensure we have the latest certificates installed before calling apt-get
RUN apt update ; apt-get install ca-certificates
RUN python3 -m pip install --upgrade pip
