# Use the official Ubuntu base image
FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install additional tools
RUN apt-get update && apt-get install -y \
    curl \
    wget \
    git \
    && rm -rf /var/lib/apt/lists/*

# Install Node.js and npm (if not already included)
RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash - \
    && apt-get install -y nodejs

# Install global npm packages
RUN npm install -g live-server prettier html-validate

# Set the default shell
SHELL ["/bin/bash", "-c"]

# Create workspace directory
RUN mkdir -p /workspaces
WORKDIR /workspaces

# Switch to vscode user
USER vscode
