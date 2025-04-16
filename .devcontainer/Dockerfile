FROM ubuntu:22.04

# Set noninteractive for automated install
ENV DEBIAN_FRONTEND=noninteractive

# Install basic tools
RUN apt update && apt install -y \
    sudo \
    curl \
    wget \
    git \
    unzip \
    nano \
    build-essential \
    libssl3 \
    libssl-dev \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

# Create a non-root user (Codespaces runs as vscode)
RUN useradd -m vscode && echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER vscode
WORKDIR /workspaces
