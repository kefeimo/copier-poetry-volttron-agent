# Copier VOLTTRON Agent

[Copier](https://github.com/copier-org/copier) template
for Python projects managed by [Poetry](https://github.com/python-poetry/poetry).

Many thanks to the project [copier poetry](https://github.com/pawamoy/copier-poetry)
for starting this project and allowing the reuse of the codebase there.  Without this
starting point the agent templates would not be what they are today!

## Features

- [Poetry](https://github.com/sdispater/poetry) setup, with pre-defined `pyproject.toml`
- Documentation built with [MkDocs](https://github.com/mkdocs/mkdocs)
  ([Material theme](https://github.com/squidfunk/mkdocs-material)
  and "autodoc" [mkdocstrings plugin](https://github.com/pawamoy/mkdocstrings))
- Pre-configured tools for code formatting, quality analysis and testing:
    - [black](https://github.com/psf/black),
    - [flake8](https://gitlab.com/pycqa/flake8) and plugins,
    - [isort](https://github.com/timothycrosley/isort),
    - [mypy](https://github.com/python/mypy),
    - [safety](https://github.com/pyupio/safety)
- Tests run with [pytest](https://github.com/pytest-dev/pytest) and plugins,
  with [coverage](https://github.com/nedbat/coveragepy) support
- Cross-platform tasks with [duty](https://github.com/pawamoy/duty)
- Support for GitHub workflow and Gitlab CI
- Python 3.8 or above
- Auto-generated `CHANGELOG.md` from git commits (using Angular message style)
- Auto-generated `CREDITS.md` from Python dependencies
- All licenses from [choosealicense.com](https://choosealicense.com/appendix/)
- Makefile for convenience

## Quick setup and usage

Make sure all the
[requirements](https://pawamoy.github.io/copier-poetry/requirements)
are met, then:

```bash
copier "https://github.com/VOLTTRON/copier-poetry-volttron-agent.git" /path/to/your/new/project
```

Or even shorter:

```bash
copier "gh:VOLTTRON/copier-poetry-volttron-agent" /path/to/your/new/project
```
