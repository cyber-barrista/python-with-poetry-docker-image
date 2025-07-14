FROM python:3.13

RUN apt-get update && apt-get install -y build-essential libssl-dev libffi-dev cargo

ENV CARGO_REGISTRIES_CRATES_IO_PROTOCOL=sparse
RUN pip install poetry==2.1.3
