FROM python:3.12-slim

RUN apt-get update && apt-get install -y build-essential libssl-dev libffi-dev curl cargo

# ENV RUSTUP_USE_HYPER=1
# RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
# ENV PATH="/root/.cargo/bin:${PATH}"

# RUN rustup toolchain install nightly

ENV CARGO_REGISTRIES_CRATES_IO_PROTOCOL=sparse
RUN pip install poetry==2.1.3
