# syntax=docker/dockerfile:1.6
FROM debian:trixie

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
  && apt-get -y dist-upgrade \
  && apt-get install -y --no-install-recommends \
  curl jq yq less neovim sqlite3 python3 python3-venv \
  build-essential file binutils fzf ripgrep bat ca-certificates git \
  && ln -sf /usr/bin/batcat /usr/local/bin/bat || true \
  && apt-get clean && rm -rf /var/lib/apt/lists/*
