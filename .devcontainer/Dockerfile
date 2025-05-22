# Use the official Rust slim image based on Debian Bookworm with Rust 1.87
# FROM rust:1.87-slim-bookworm
FROM mcr.microsoft.com/devcontainers/rust:latest

# Install additional dependencies for development
RUN sudo apt-get update && sudo apt-get install -y \
    build-essential \
    curl \
    git \
    pkg-config \
    libssl-dev \
    python3-lldb \
    && rm -rf /var/lib/apt/lists/*

# Install rustup components and tools
RUN rustup component add cargo clippy rust-analyzer rust-docs rust-src rust-std rustc rustfmt \
    && rustup update

# Install common Rust tools
RUN cargo install cargo-watch

# Set the working directory
WORKDIR /workspaces

