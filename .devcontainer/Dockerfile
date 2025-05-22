# Use the latest Microsoft devcontainer image for Rust
FROM mcr.microsoft.com/devcontainers/rust:latest

# Install specified dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    git \
    pkg-config \
    libssl-dev \
    && rm -rf /var/lib/apt/lists/*

# Install additional Rust tools (optional, customizable)
RUN cargo install cargo-watch

# Set the working directory
WORKDIR /workspaces

# Ensure the codespace user has correct permissions
USER vscode
RUN chown -R vscode:vscode /workspaces

# Set the default command
CMD ["bash"]
