---
title: "Project Standards"
summary: Deliver high quality projects using automation.
tags:
- Automation
- Project management
date: 2020-01-05T11:34:59-06:00
---

## Objectives

The goal of this document is to provide the developers with clear guidelines to manage their projects.

It is important to emphasize that the usage of specific tools will not be enforced, except for special cases (i.e. docker for containers), but instead the concepts will have to be implemented (i.e. projects must provide unit tests).

To allow the developers to start quickly, generators will be provided when applicable.

## Standards

* Service API must be defined using the [OpenAPI 3+ specification](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md)
  * Zalando provides very good [RESTful API Guidelines](https://opensource.zalando.com/restful-api-guidelines/) worth following
* Projects must provide a way to build artifacts using standard tools (i.e. no custom scripts made for a specific machine/environment)
  * a package or binary depending on the language
  * a docker image
* Projects must comply with CI tasks
  * Formatter
  * Linters
    * Code
    * Docstrings
  * Static analyzers
  * Documentation
  * Unit/Feature tests
  * Coverage
    * Reaching 100% coverage is not the end goal
    * Must never regress
    * Think about your teammates who worked on increasing this coverage
    * Use online services like <https://coveralls.io> or <https://codecov.io>
    * Use feature tests
      * Try to cover 100% of use cases
        * This is more important the unit test coverage
        * It will end up increasing unit test coverage anywway
* Projects must include a Changelog following the "Keep a Changelog" recommendation (<https://keepachangelog.com/en/1.0.0>)
* Project must adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) 
  * Or [Calendar Versioning](https://calver.org>) if it makes more sense.
* Projects must use Issues and Pull Request templates
* Projects must use meaningful labels
* Projects must be documented
* Projects must automate all their maintenance tasks
  * Must ensure reproducibility
  * A Makefile or a package.json at the root of the project is a good example of how to automate maintenance tasks. The commands must be backed by a set of bash scripts (instead of being written inline).

## Recommendation per language

Recommendations are provided to help the developers choose the right tool for the right task without spending too much time on the research phase.

### All

* [Changelog](https://github.com/scrapd/scrapd/blob/master/CHANGELOG.md)
* Project templates
  * Github
    * [Issues](https://github.com/scrapd/scrapd/blob/master/.github/ISSUE_TEMPLATE.md)
    * [Pull Requests](https://github.com/scrapd/scrapd/blob/master/.github/PULL_REQUEST_TEMPLATE.md)
    * [Contributing](https://github.com/scrapd/scrapd/blob/master/.github/CONTRIBUTING.rst)
* [EditorConfig](https://editorconfig.org/) to standardize editor configurations.

### Python

* Project source layout

```bash
.
├── CHANGELOG.md
├── Dockerfile
├── LICENSE
├── README.rst
├── assets
│   └── logos
├── code-of-conduct.md
├── contrib
│   └── scrapd-complete.sh
├── contributors.md
├── docs
│   └── source
├── noxfile.py
├── requirements-dev.txt
├── requirements.txt
├── scrapd
│   ├── __init__.py
│   ├── cli
│   ├── core
│   └── main.py
├── setup.cfg
├── setup.py
├── tasks.py
└── tests
    ├── __init__.py
    ├── core
    ├── data
    ├── features
    ├── mock_data.py
    ├── step_defs
    └── test_common.py
```

* Packaging
  * Use [PBR](https://docs.openstack.org/pbr/latest/) to create a package
    * Package the application as a [wheel](https://pypi.org/project/wheel/) (.whl)
  * _Alternative_: [Poetry](https://github.com/sdispater/poetry) (does dependency+package management)
* CI tasks
  * Formatter: [Black](https://github.com/python/black)
    * _Alternative_: [YAPF](https://github.com/google/yapf)
  * Linters
    * [pycodestyle](https://github.com/PyCQA/pycodestyle)
    * [pydocstyle](https://github.com/PyCQA/pydocstyle)
  * Static analyzers
    * [PyFlakes](https://github.com/PyCQA/pyflakes)
    * [Pylint](https://github.com/PyCQA/pylint)
    * [McCabe's script](https://github.com/PyCQA/mccabe)
  * Documentation: [Sphinx](http://www.sphinx-doc.org/en/master/)
  * Unit/Feature tests
    * [Pytest](https://docs.pytest.org/en/latest/) with the following plugins
      * [pytest-asyncio](https://github.com/pytest-dev/pytest-asyncio)
      * [pytest-bdd](https://github.com/pytest-dev/pytest-bdd)
      * [pytest-cov](https://github.com/pytest-dev/pytest-cov)
      * [pytest-mock](https://github.com/pytest-dev/pytest-mock/)
      * [pytest-rerunfailures](https://github.com/pytest-dev/pytest-rerunfailures)
      * [pytest-socket](https://github.com/miketheman/pytest-socket)
      * [pytest-xdist](https://github.com/pytest-dev/pytest-xdist)
    * Coverage: [coverage.py](https://github.com/nedbat/coveragepy)
* Maintenance tasks automation: [Invoke](https://github.com/pyinvoke/invoke) + [Nox](https://github.com/theacodes/nox)
  * _Alternative_: [Makefile](https://github.com/scrapd/scrapd/blob/master/Makefile)
  * _Alternative_: [Tox](https://tox.readthedocs.io/en/latest/)

#### Remarks

* [Flake8](https://github.com/PyCQA/flake8) can be used as a wrapper for PyFlakes, pycodestyle, and Ned Batchelder's McCabe script.

## Node.js/React

* CI Tasks
  * Formatter: [Prettier](https://prettier.io/)
  * Linters: [ESLint](https://eslint.org/)
  * Unit tests:
    * Framework: [Jest](https://jestjs.io/)
    * Coverage: [Jest](https://jestjs.io/)
* Maintenance tasks automation
  * `package.json`: https://github.com/scrapd/scrapdviz/blob/master/package.json

## Go

* Formatter (built-in): `goimports`
* Linters: [golangci-lint](https://golangci.com/)
* Documentation (built-in): `godoc`
* Unit tests:
  * Framework: go test (built-in): `go test -v -cover -coverprofile=coverage.out  ./...`
  * Coverage: go tool (built-in): `go tool cover -html=coverage.out`
* Maintenance tasks automation
  * [Go Task](https://taskfile.dev)
  * _Alternative_: [Mage](https://github.com/magefile/mage)

## Ruby

* Formatter: [rubocop](https://www.rubocop.org/en/stable/)
* Linters: [rubocop](https://www.rubocop.org/en/stable/)
* Static analyzers: [rubocop](https://www.rubocop.org/en/stable/)
* Documentation: [yard](https://yardoc.org/)
* Unit test: [rspec](https://rspec.info/)
* Coverage: [simplecov](https://github.com/colszowka/simplecov)
