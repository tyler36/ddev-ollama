[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/tyler36/ollama/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/tyler36/ollama/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/tyler36/ollama)](https://github.com/tyler36/ollama/commits)
[![release](https://img.shields.io/github/v/release/tyler36/ollama)](https://github.com/tyler36/ollama/releases/latest)

# DDEV Ollama

## Overview

This add-on integrates [Ollama](https://ollama.com/) into your [DDEV](https://ddev.com/) project.

[Ollama](https://ollama.com/) allows developers to run LLMs locally.

## Installation

```bash
ddev add-on get tyler36/ollama
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Ollama |
| `ddev logs -s ollama` | Check Ollama logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.ollama --ollama-docker-image="ollama/ollama:latest"
ddev add-on get tyler36/ollama
ddev restart
```

Make sure to commit the `.ddev/.env.ollama` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `OLLAMA_DOCKER_IMAGE` | `--ollama-docker-image` | `ollama/ollama:latest` |

> [!tip]
> If you do not require GPU support, it is recommended to use [`alpine/ollama`](https://hub.docker.com/r/alpine/ollama)
> It is significantly smaller, however, it be a week or 2 out of sync with the latest `ollama/ollama` image.

## Credits

**Contributed and maintained by [@tyler36](https://github.com/tyler36)**
