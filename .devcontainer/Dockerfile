# Scholar Dev Hub — Reproducible AI development environment
# Base: Microsoft's devcontainers Python image (Debian 12 / bookworm).
# Pre-installs everything a modern AI coding agent needs to run out of the box:
# Python, build tools, Git, curl/jq/ripgrep, and an isolated uv install.

FROM mcr.microsoft.com/devcontainers/python:3.12

# Core system dependencies
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
        curl \
        wget \
        git \
        gnupg \
        jq \
        ripgrep \
        ca-certificates \
        build-essential \
        file \
        unzip \
        less \
        sudo \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# A fast, modern Python package manager (https://docs.astral.sh/uv)
# Used by most agent and RAG workflows to install deps in seconds.
RUN curl -LsSf https://astral.sh/uv/install.sh | sh \
    && mv /root/.local/bin/uv /usr/local/bin/uv \
    && mv /root/.local/bin/uvx /usr/local/bin/uvx

# A small, opinionated set of Python utilities helpful for AI/dev work
RUN pip install --no-cache-dir \
        "ruff" \
        "black" \
        "ipykernel" \
        "jupyterlab"

# Helpful defaults so coding agents (Claude Code, Aider, Gemini CLI, etc.)
# find a sensible environment without per-project setup.
ENV PYTHONUNBUFFERED=1 \
    SHELL=/bin/bash \
    LANG=C.UTF-8 \
    LC_ALL=C.UTF-8

# A non-root user (matches the devcontainers base image convention)
USER vscode

WORKDIR /workspace