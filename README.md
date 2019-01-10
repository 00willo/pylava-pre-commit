# Pylava pre-commit hook for the pre-commit framework

Use this git hook with [pre-commit](https://pre-commit.com/) to run the awesome [pylama](https://github.com/pylava/pylava) tool.

## Setup

If `pre-commit` is not already installed, then you can do so by running this command:

```bash
pip install pre-commit
```
See the `pre-commit` [documentation](https://pre-commit.com/#install) for further details.

Configure this hook by editting your `.pre-commit-config.yml` file, located in the root of your repository

```yaml
repo:
  - repo: https://github.com/00willo/pylava-pre-commit
    rev: 0.1.0
    hooks:
      - id: pylava
```

You can immediately install the hook by issuing this command
```
pre-commit install-hooks
```

## Usage

Pylava will then run as per a normal git hook when you commit or you can execute the pre-commit hook manually

```bash
pre-commit run pylava --files src
```
See the `pre-commit` [documentation](https://pre-commit.com/#pre-commit-run) for further details.
