# Use the official Ubuntu 20.04 image from the Docker Hub
FROM ubuntu:20.04

# Set environment variables to avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Update the package list and install any updates
RUN apt-get update && apt-get upgrade -y

# Install common tools, utilities, and virtualization packages
RUN apt-get install -y \
    build-essential \
    curl \
    git \
    vim \
    wget \
    sudo \
    lsb-release \
    software-properties-common \
    qemu-kvm \
    libvirt-daemon-system \
    libvirt-clients \
    bridge-utils \
    virt-manager \
    cpu-checker

# Enable KVM and set up the working directory
RUN systemctl enable libvirtd

# Set up the working directory
WORKDIR /workspace

# Set the default command
CMD ["bash"]
