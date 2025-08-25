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

`ddev ollama` is a helper command allowing developers to interact with the Ollama service.
The table below disable some commonly-used commands. Type `ddev ollama --help` to see all available commands.

| Command                   | Description                                                              |
| ------------------------- | ------------------------------------------------------------------------ |
| `ddev ollama run <model>` | Run a model. Models will automatically download if not available locally |
| `ddev ollama stop`        | Stop a running model                                                     |
| `ddev ollama list`        | List models                                                              |
| `ddev ollama ps`          | List running models                                                      |
| `ddev ollama --help`      | Show available commands                                                  |

### Other Commands

| Command               | Description                                   |
| --------------------- | --------------------------------------------- |
| `ddev describe`       | View service status and used ports for Ollama |
| `ddev logs -s ollama` | Check Ollama logs                             |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.ollama --ollama-docker-image="ollama/ollama:latest"
ddev add-on get tyler36/ollama
ddev restart
```

Make sure to commit the `.ddev/.env.ollama` file to version control.

All customization options (use with caution):

| Variable              | Flag                    | Default                |
| --------------------- | ----------------------- | ---------------------- |
| `OLLAMA_DOCKER_IMAGE` | `--ollama-docker-image` | `ollama/ollama:latest` |

## Credits

**Contributed and maintained by [@tyler36](https://github.com/tyler36)**
