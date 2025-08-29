# syntax=docker/dockerfile:1

# Base: Official Dev Containers Python image (Debian Bookworm)
FROM mcr.microsoft.com/devcontainers/python:3.12-bookworm

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# Install curl and uv (installed to /usr/local/bin)
ENV UV_NO_ANALYTICS=1
RUN apt-get update \
    && apt-get install -y --no-install-recommends curl ca-certificates \
    && rm -rf /var/lib/apt/lists/* \
    # Install uv
    && export UV_INSTALL_DIR=/usr/local/bin \
    && curl -LsSf https://astral.sh/uv/install.sh | sh \
    && uv --version

# Default workdir set by base image: /workspaces/${localWorkspaceFolderBasename}
# The devcontainer.json will create a local .venv and install deps with `uv sync`.
