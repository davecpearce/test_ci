FROM mcr.microsoft.com/vscode/devcontainers/python:0-3.10

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN apt update \
    && sudo apt install -y libpcap-dev vim curl jq \
    && mkdir -p /opt

WORKDIR /workspaces/test_ci
COPY requirements.txt ./
RUN python3 -m pip install -r requirements.txt

ENV SHELL /bin/bash
