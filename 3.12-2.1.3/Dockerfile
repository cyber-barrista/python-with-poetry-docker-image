FROM --platform=$BUILDPLATFORM python:3.12-slim

RUN apt-get update && apt-get install -y build-essential libssl-dev libffi-dev cargo
RUN pip install poetry==2.1.3
