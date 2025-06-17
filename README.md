# Python project template with Copier and Make
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-border.json)](https://github.com/copier-org/copier)

## Usage

### Install

```shell
uv tool install --with jinja2-shell-extension --with jinja2-time copier
```

### Seed new project

```shell
uvx copier copy --trust --vcs-ref main gh:makukha/copython .
just seed sync
just pre-merge
```

### Test template locally

```shell
uvx copier copy --trust --vcs-ref $(git rev-parse --abbrev-ref HEAD) . .tmp
cd .tmp
just seed sync
just pre-merge
```

Update local testing instance:

```shell
uvx copier copy --trust --vcs-ref $(git rev-parse --abbrev-ref HEAD) --data-file .tmp/.copier-answers.yml --overwrite . .tmp
```
