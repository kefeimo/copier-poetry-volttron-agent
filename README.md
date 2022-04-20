# Copier VOLTTRON Agent

[Copier](https://github.com/copier-org/copier) template
for Python projects managed by [Poetry](https://github.com/python-poetry/poetry).

Many thanks to the project [copier poetry](https://github.com/pawamoy/copier-poetry)
for starting this project and allowing the reuse of the codebase.  Without this
starting point the agent templates would not be what they are today!


# Quick setup and usage

## Prerequisites

* [git v2](https://git-scm.com/)
* Python 3
* [Copier](https://copier.readthedocs.io/en/stable/)


Install all the
[requirements](https://pawamoy.github.io/copier-poetry/requirements).

NOTE: We highly recommend using the copier as a CLI app. To install copier and use it as a CLI tool,
you will need `pipx` installed. However, you might not be able to install copier via `pipx` due to a [bug in copier](https://github.com/copier-org/copier/issues/574).

If you are having problems installing copier with `pipx`, try installing copier using the following [workaround](https://github.com/copier-org/copier/issues/574#issuecomment-1046708983):

```shell
pipx install copier
pipx inject copier "MarkupSafe<2.1.0"
```


## Usage

Use the copier CLI tool to create an agent project from the Volttron Copier templates. The command
takes the form of:

`copier <URL to copier template repo> <path to agent project on local machine>`

The following is an example:
```bash
copier "https://github.com/VOLTTRON/copier-poetry-volttron-agent.git" /path/to/your/new/project
```

Or even shorter:

```bash
copier "gh:VOLTTRON/copier-poetry-volttron-agent" /path/to/your/new/project
```

NOTE: By default, copier use the latest release found in the template git tags.
want to use a specific template version, use the `--vcs-ref` flag, which takes a commit hash associated with your desired
template version. See [documentation for this flag](https://copier.readthedocs.io/en/latest/configuring/#vcs_ref).


# Features

- [Poetry](https://github.com/sdispater/poetry) setup, with pre-defined `pyproject.toml`
- Documentation built with [Sphinx](https://www.sphinx-doc.org/en/master/)
- Pre-configured tools for code formatting, quality analysis and testing:
    - [yapf](https://github.com/google/yapf)
    - [isort](https://github.com/timothycrosley/isort),
    - [mypy](https://github.com/python/mypy),
    - [safety](https://github.com/pyupio/safety)
- Tests run with [pytest](https://github.com/pytest-dev/pytest) and plugins,
  with [coverage](https://github.com/nedbat/coveragepy) support
- Support for GitHub workflow and Gitlab CI
- Python 3.8 or above
- Auto-generated `CHANGELOG.md` from git commits (using Angular message style)
- All licenses from [choosealicense.com](https://choosealicense.com/appendix/)


# Development

## Copier Workflow diagram

![Copier sequence diagram](copier_workflow.png)
