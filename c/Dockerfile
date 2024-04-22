FROM alpine:latest

RUN apk add build-base

WORKDIR /app

COPY ./ /app

RUN gcc ./src/main.c
