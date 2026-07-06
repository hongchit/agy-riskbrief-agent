FROM mcr.microsoft.com/devcontainers/python:3-3.14-trixie

USER root

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        bash \
        ca-certificates \
        curl \
    && rm -rf /var/lib/apt/lists/*

USER vscode

ENV PATH="/home/vscode/.local/bin:${PATH}"

RUN curl -fsSL https://antigravity.google/cli/install.sh | bash \
    && agy --version
