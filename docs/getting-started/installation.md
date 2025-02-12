# Installation

This page covers the installation of DipDup in different environments.

## Host requirements

A Linux environment with **Python 3.10** installed is required to use DipDup.

Minimum hardware requirements are 256 MB RAM, 1 CPU core, and some disk space for the database. RAM requirements increase with the number of indexes.

### Non-Linux environments

Other UNIX-like systems (macOS, FreeBSD, etc.) should work but are not supported officially.

DipDup currently doesn't work in Windows environments due to incompatibilities in libraries it depends on. Please use WSL or Docker.

We aim to improve cross-platform compatibility in future releases ([issue](https://github.com/dipdup-net/dipdup-py/pull/358)).

> 💡 **SEE ALSO**
>
> * {{ #summary advanced/performance.md }}
> * [What is the Windows Subsystem for Linux?](https://docs.microsoft.com/en-us/windows/wsl/about)

## Local installation

### Interactively (recommended)

You can initialize a hello-world project interactively by choosing configuration options in the terminal. Install [`cookiecutter`](https://cookiecutter.readthedocs.io/en/stable/README.html) package systemwide, then run:

```shell
cookiecutter https://github.com/dipdup-net/cookiecutter-dipdup
```

### Poetry

We advise using the [Poetry](https://python-poetry.org) package manager for new projects. However, it's not a requirement. If you prefer pdb, piptools, pipenv or other tools — use them instead.

```shell
# Create a new project
mkdir my-indexer; cd my-indexer
poetry init --python ">=3.10,<3.11"
# Add dipdup as a dependency
poetry add dipdup
# Enter the virtualenv
poetry shell
```

> 💡 **SEE ALSO**
>
> * [Poetry documentation](https://python-poetry.org/docs/)

### pip

Create a new virtual environment and install DipDup in it.

```shell
python -m venv .venv
source .venv/bin/activate
pip install dipdup
```

## Docker

See {{ #summary deployment/docker.md }} page.
