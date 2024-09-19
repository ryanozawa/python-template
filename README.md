# python-template
Template repository with uv, pre-commit and ruff


## Get Started

To start development on this project, it is suggested to do the following to get past the majority of first time errors.

```bash
# to install uv
curl -LsSf https://astral.sh/uv/0.4.0/install.sh | sh
# to install dependencies
uv sync --all-extras --frozen

## HIGHLY SUGGESTED: install pre-commit hooks
uv run pre-commit install
```

## Code

### Code Quality

This repository uses linters, formatters, and static analysis tools at time of commit thanks to [pre-commit](https://pre-commit.com/). These jobs are also run in GitHub Actions to enforce the quality.

Main hooks involve:

- [ruff](https://docs.astral.sh/ruff/)
- [mypy](https://www.mypy-lang.org/)

If there are any problems with those, check out the respective documentation for those tools.

<details>
  <summary><strong>Make sure your pre-commit is installed before dev work.</strong></summary>

  ```bash
  uv sync --with dev --frozen
  uv run pre-commit install
  ```
</details>


### Virtual Environment

Use [uv](https://docs.astral.sh/uv/) for the virtual environment management and strict hash pinning of the packages we use.

The packages and configuration of most tools resides in `pyproject.toml`.

## Changelog

We use [changie](https://changie.dev/) to manage the changelog.

To create a new changelog entry, run the following command:

```bash
changie new
```

This will create a new changelog entry in the `.changes/unreleased` directory.

For more information on how to use changie, please refer to the [official documentation](https://changie.dev/guide/quick_start/).