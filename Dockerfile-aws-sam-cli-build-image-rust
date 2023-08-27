from  public.ecr.aws/sam/build-provided.al2

env RUSTUP_HOME=/usr/local/rustup
env CARGO_HOME=/usr/local/cargo
env PATH=/usr/local/cargo/bin:$PATH
run curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

run curl https://ziglang.org/download/0.11.0/zig-linux-x86_64-0.11.0.tar.xz | tar -xJ -C /usr/local/bin
env PATH=$PATH:/usr/local/bin/zig-linux-x86_64-0.11.0

run cargo install cargo-lambda

env HOME=/tmp

run chmod -R a+rw /usr/local/cargo/registry

env SAM_CLI_TELEMETRY=0
