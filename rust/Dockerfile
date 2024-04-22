FROM rust:1.77-alpine

RUN apk add --no-cache build-base libffi-dev
RUN rustup component add rustfmt

WORKDIR /app

COPY ./ /app

RUN cargo build --release
