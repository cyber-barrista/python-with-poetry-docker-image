# syntax=docker/dockerfile:experimental
FROM python:3.13-slim

RUN apt-get update && apt-get install -y build-essential libssl-dev libffi-dev curl

RUN --security=insecure curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sed 's#/proc/self/exe#$SHELL#g' | sh -s -- -y --profile minimal --default-toolchain nightly
ENV PATH="/root/.cargo/bin:${PATH}"

RUN rustup toolchain install nightly

ENV CARGO_REGISTRIES_CRATES_IO_PROTOCOL=sparse
RUN pip install poetry==2.1.3
