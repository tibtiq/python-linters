# Overview

This repo contains my configs to python linters.

It currently uses [ruff](https://www.google.com/search?client=firefox-b-1-d&q=python+ruff) as the formatter and linter.

# How to setup github action in a new repo

- Create a github workflow `.github\workflows\ci.yml` in the repo
- Add the following code to the file

```
name: CI

on:
  workflow_dispatch: # allows manual trigger
  push:
    branches: [ main ] # Only runs when code is merged/pushed directly to main
  pull_request:
    branches: [ main ] # Only runs when a PR targets the main branch

jobs:
  formatter-and-linter:
    uses: tibtiq/python-linters/.github/workflows/formatter_and_linter.yml@main

  tests:
    uses: tibtiq/python-linters/.github/workflows/tests.yml@main

```
