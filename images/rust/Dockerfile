# Use the official Rust image
FROM rust:1.80.1-alpine

# Set the working directory
RUN adduser --home /sandbox --disabled-password sandbox

RUN apk add --no-cache inotify-tools

COPY run_rust /usr/local/bin/run_rust
RUN chmod +x /usr/local/bin/run_rust


USER sandbox
WORKDIR /sandbox

ENV TMPDIR=/sandbox