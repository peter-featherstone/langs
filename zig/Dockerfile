FROM debian:stable-slim

ARG ZIG_VERSION=0.13.0
ARG TARGETARCH

RUN apt-get update && apt-get install -y curl xz-utils && rm -rf /var/lib/apt/lists/*

# Map Docker arch names -> Zig arch names
RUN if [ "$TARGETARCH" = "arm64" ]; then \
        export ZIG_ARCH="aarch64"; \
    else \
        export ZIG_ARCH="$TARGETARCH"; \
    fi \
    && curl -L "https://ziglang.org/download/${ZIG_VERSION}/zig-linux-${ZIG_ARCH}-${ZIG_VERSION}.tar.xz" -o zig.tar.xz \
    && tar -xf zig.tar.xz \
    && mv zig-linux-${ZIG_ARCH}-${ZIG_VERSION} /zig \
    && rm zig.tar.xz

ENV PATH="/zig:$PATH"
WORKDIR /app
