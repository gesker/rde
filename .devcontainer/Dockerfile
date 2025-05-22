FROM mcr.microsoft.com/devcontainers/rust:latest

# Include lld linker to improve build times either by using environment variable
# RUSTFLAGS="-C link-arg=-fuse-ld=lld" or with Cargo's configuration file (i.e see .cargo/config.toml).
RUN apt-get update && apt-get upgrade -y && export DEBIAN_FRONTEND=noninteractive \
   && apt-get -y install clang lld \
   && apt-get autoremove -y && apt-get clean -y

RUN rustup component add cargo clippy rust-analyzer rust-docs rust-src rust-std rustc rustfmt && rustup update && cargo install cargo-watch && cargo --version && rustc --version
