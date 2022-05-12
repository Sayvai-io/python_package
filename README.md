```

   ___         _    _                     _____                         _         _
  / _ \ _   _ | |_ | |__    ___   _ __   /__   \ ___  _ __ ___   _ __  | |  __ _ | |_  ___  ___
 / /_)/| | | || __|| '_ \  / _ \ | '_ \    / /\// _ \| '_ ` _ \ | '_ \ | | / _` || __|/ _ \/ __|
/ ___/ | |_| || |_ | | | || (_) || | | |  / /  |  __/| | | | | || |_) || || (_| || |_|  __/\__ \
\/      \__, | \__||_| |_| \___/ |_| |_|  \/    \___||_| |_| |_|| .__/ |_| \__,_| \__|\___||___/
        |___/                                                   |_|

```
<!-- source - https://patorjk.com/software/taag/#p=display&h=1&f=Ogre&t=Python%20Templates -->

[![License](https://img.shields.io/badge/License-Creative%20Commons%20Zero%20v1.0-informational?style=flat)](./LICENSE)
[![Documentation: Sphinx](https://img.shields.io/badge/Documentation-Sphinx-08476D?style=flat)](https://www.sphinx-doc.org/en/master/)
[![codecov](https://codecov.io/gh/crabtr26/python_templates/branch/main/graph/badge.svg?token=RRYTJVFDG3)](https://codecov.io/gh/crabtr26/python_templates)
[![Code style: black](https://img.shields.io/badge/code%20style-black-151515?style=flat)](https://github.com/psf/black)
[![Imports: isort](https://img.shields.io/badge/%20imports-isort-EE8236?style=flat)](https://pycqa.github.io/isort/)


## Description
A basic template which includes proper package structure, imports, and a working `setup.py`.
Includes flake8, pylint, isort, and pytest settings with configurations compatible with
the black autoformatter. Pylint settings are based on the Google style standards for python
and adapted for black compatibility. Package metadata and dependency information is stored
in the pyproject.toml.

## Setup
Using `virtualenv`:
```
git clone https://github.com/crabtr26/python_templates.git
cd python_templates
virtualenv venv
source venv/bin/activate
pip install .
```

## Usage
From the CLI:
```
pytemplates --hello {name}
pytemplates --goodbye {name}
pytemplates --test
```

From a `.py` file:
```python
import mypackage
mypackage.greet(user="Jacob")
mypackage.wish_farewell(user="Jacob")
```

## Development Setup
Using `virtualenv`:
```
git clone https://github.com/crabtr26/python_templates.git
cd python_templates
virtualenv venv
source venv/bin/activate
pip install -e .[dev]
```

## Testing
To run the tests locally using the development environment:
```
cd python_templates
pytest
```

## Documentation
To build and view the documentation locally using the development environment:
```
cd docs
make html
google-chrome build/html/index.html
```
