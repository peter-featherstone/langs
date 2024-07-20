FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y binutils
RUN apt-get install -y nasm

WORKDIR /app

COPY ./ /app

RUN nasm -f elf64 -o ./src/main.o ./src/main.asm
RUN ld ./src/main.o
