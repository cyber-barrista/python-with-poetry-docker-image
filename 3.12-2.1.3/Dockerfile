FROM python:3.12-slim

RUN apt-get update && apt-get install -y build-essential libssl-dev libffi-dev cargo git

RUN mkdir -p ~/.cargo/registry/index && cd ~/.cargo/registry/index && git clone --bare https://github.com/rust-lang/crates.io-index.git github.com-1285ae84e5963aae

RUN pip install poetry==2.1.3
