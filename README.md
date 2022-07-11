<p align="center">
  <a href="https://user-images.githubusercontent.com/20674972/178172752-abd4497d-6a0e-416b-9eef-1b1c0dca8477.png">
    <img src="https://user-images.githubusercontent.com/20674972/178172752-abd4497d-6a0e-416b-9eef-1b1c0dca8477.png" alt="Pytemplates Banner" style="width:100%;">
  </a>
</p>

<p align="center">
  <a href="https://github.com/PyTemplate/python_package/actions/workflows/test.yaml">
    <img src="https://github.com/PyTemplate/python_package/actions/workflows/test.yaml/badge.svg" alt="Test status">
  </a>

  <a href="https://github.com/PyTemplate/python_package/actions/workflows/lint.yaml">
    <img src="https://github.com/PyTemplate/python_package/actions/workflows/lint.yaml/badge.svg" alt="Linting status">
  </a>

  <a href="https://results.pre-commit.ci/latest/github/PyTemplate/python_package/main">
    <img src="https://results.pre-commit.ci/badge/github/PyTemplate/python_package/main.svg" alt="pre-commit.ci status">
  </a>

  <a href="https://codecov.io/gh/PyTemplate/python_package">
    <img src="https://codecov.io/gh/PyTemplate/python_package/branch/main/graph/badge.svg?token=HG1NQ8HRA4" alt="Code coverage status">
  </a>

  <a href="https://pypi.org/project/pytemplates-pypackage/">
    <img src="https://badge.fury.io/py/pytemplates_pypackage.svg" alt="PyPI version">
  </a>
</p>

## Description

A basic python package template which includes proper package structure with a functioning package installation. The package is built using poetry; metadata and dependency information is stored in the pyproject.toml. This template includes flake8, pylint, isort, and pytest settings with configurations compatible with the black autoformatter. Pylint settings are based on the Google style standards for python and adapted for black compatibility.  Testing is automated using github workflows, codecov.io, and pre-commit.ci. Application deployment is managed using multi-staged docker builds for fast develop/deploy cycles.

## Installation

To install the package using `pip`:

```bash
pip install pytemplates_pypackage
```

To add the package as a dependency using `poetry`:

```bash
poetry add pytemplates_pypackage
```

## Usage

From a `.py` file:

```python
import pytemplates_pypackage
print(pytemplates_pypackage.__version__)
pytemplates_pypackage.greet(user="Jacob")

from pytemplates_pypackage import wish_farewell
wish_farewell(user="Jacob")
```

## Developer Setup

Install the package using `poetry`:

```bash
poetry install
```

Install optional dependencies using the `--extras` flag:

```bash
poetry install --extras={environment}
```

### Environments

```python
test = [
    "pytest",
    "pytest-cov",
]

lint = [
    "black",
    "isort",
    "flake8",
    "pylint",
    "mypy",
    "pre-commit",
]

docs = [
    "Sphinx",
    "sphinx-rtd-theme",
]

# Includes all optional dependencies
dev = [
    "pytest",
    "pytest-cov",
    "black",
    "isort",
    "flake8",
    "pylint",
    "mypy",
    "pre-commit",
    "Sphinx",
    "sphinx-rtd-theme",
    "bump2version",
]
```

## Commands

`make clean` - Remove all build, testing, and static documentation files.

`make lint` - Run the linting tools. Includes pre-commit hooks, black, isort, flake8, pylint, and mypy.

`make test` - Run the tests using pytest.

`make check` - Run the lint, test, and clean commands.

`make gen-docs` - Generate Sphinx HTML documentation.

`make docs` - Generate Sphinx HTML documentation and serve it to the browser.

`make pre-release` - Bump the version and create the release tag.

`make release` - Push the release tag and trigger the release pipeline.

## Workflows

`lint` - Run the linting tools on every push/pull_request to the *main* branch. Includes pre-commit hooks, black, isort, flake8, pylint, and mypy.

`test` - Run the tests on every push/pull_request to the *main* branch. Writes a coverage report using pytest-cov and uploads it to codecov.io.

`build-and-release` - Build a package distribution, create a github release, and publish the distribution to PyPI on every tag creation. Linting and testing steps must pass before the build process can begin. Sphinx documentation is automatically published to the *sphinx-docs* branch and hosted on github pages.

## File Tree

```bash
.
├── docs/
├── LICENSE
├── Makefile
├── poetry.lock
├── pyproject.toml
├── README.md
├── src
│   └── pytemplates_pypackage
│       ├── core
│       │   ├── __init__.py
│       │   ├── module1.py
│       │   └── module2.py
│       ├── __init__.py
│       └── __version__.py
└── tests
    ├── __init__.py
    ├── test_module1.py
    └── test_module2.py
```
