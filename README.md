# Just-based Python template
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-border.json)](https://github.com/copier-org/copier)

## Usage

### Seed new project

```shell
uv tool install --with jinja2-shell-extension --with jinja2-time copier
uvx copier copy --trust --vcs-ref main gh:makukha/copier-python .
just init
```

### Test template locally

```shell
uvx copier copy --trust --vcs-ref main . .tmp
cd .tmp
just init
just sync
just pre-merge
```
