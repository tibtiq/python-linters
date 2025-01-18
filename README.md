# Overview

This repo contains my configs to python linters.

It currently uses [ruff](https://www.google.com/search?client=firefox-b-1-d&q=python+ruff) as the formatter and linter.

# How to setup github action in a new repo

- Create a github workflow `.github\workflows\ci.yml` in the repo
- Add the following code to the file

```
name: CI

on:
  # allows manual trigger
  workflow_dispatch:
  pull_request:

jobs:
  formatter-and-linter:
    uses: tibtiq/python-linters/.github/workflows/formatter_and_linter.yml@main
```
