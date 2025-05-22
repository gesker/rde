
FROM mcr.microsoft.com/devcontainers/rust:latest

RUN sudo apt-get update && sudo apt-get -y upgrade && sudo apt-get -y install \
    build-essential \
    curl \
    git \
    libssl-dev \
    lldb \
    pkg-config \
    wget \
    && rm -rf /var/lib/apt/lists/*

RUN rustup component add cargo clippy rust-analyzer rust-docs rust-src rust-std rustc rustfmt && rustup update && cargo install cargo-watch && cargo --version && rustc --version
