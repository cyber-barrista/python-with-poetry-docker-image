FROM --platform=$BUILDPLATFORM ubuntu:24.04 AS index-fetcher

RUN apt-get update && apt-get install -y  git

RUN git clone --bare https://github.com/rust-lang/crates.io-index.git github.com-1285ae84e5963aae


FROM python:3.12-slim

USER root

RUN apt-get update && apt-get install -y build-essential libssl-dev libffi-dev cargo git

RUN mkdir -p /root/.cargo/registry/index
COPY --from=index-fetcher github.com-1285ae84e5963aae /root/.cargo/registry/index

RUN pip install poetry==2.1.3
