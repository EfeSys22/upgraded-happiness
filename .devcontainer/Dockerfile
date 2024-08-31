# Use the official Ubuntu 20.04 image from the Docker Hub
FROM ubuntu:20.04

# Set environment variables to avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Update the package list and install necessary packages
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y \
    curl \
    sudo \
    qemu-kvm \
    libvirt-daemon-system \
    libvirt-clients \
    bridge-utils \
    cpu-checker && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Enable KVM and set up the working directory
RUN systemctl enable libvirtd

# Set up the working directory
WORKDIR /workspace

# Set the default command
CMD ["bash"]
