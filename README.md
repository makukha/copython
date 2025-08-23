# Python project template with Copier and Make
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-border.json)](https://github.com/copier-org/copier)

## Usage

### Install

```shell
uv tool install copier --with jinja2-shell-extension --with jinja2-time
```

### Seed new project

```shell
uvx copier copy --trust --vcs-ref main gh:makukha/copython .
make init
just pre-merge
```

### Test template locally

```shell
uvx copier copy --trust --vcs-ref HEAD . .tmp
cd .tmp
make init
just pre-merge
```

Update local testing instance:

```shell
uvx copier copy --trust --vcs-ref HEAD --data-file .tmp/.copier-answers.yml --overwrite . .tmp
```
