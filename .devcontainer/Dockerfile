FROM mcr.microsoft.com/devcontainers/python:dev-3.13-bullseye

COPY --from=ubuntu:24.04 /etc/skel/.bashrc /home/vscode/.bashrc
RUN chown vscode:vscode /home/vscode/.bashrc

RUN apt-get update -y \
    && apt-get install -y \
    git \
    vim \
    make \
    && apt-get clean

# node22のインストール
RUN curl -fsSL https://deb.nodesource.com/setup_22.x | bash - \
    && apt-get update -y \
    && apt-get install -y nodejs \
    && npm install -g npm@latest

# bunのインストール
RUN npm install -g bun
