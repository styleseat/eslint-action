# Eslint Annotate

![Unit Tests](https://github.com/a-b-r-o-w-n/eslint-action/workflows/Unit%20Tests/badge.svg)
[![Coverage Status](https://coveralls.io/repos/github/a-b-r-o-w-n/eslint-action/badge.svg?branch=main)](https://coveralls.io/github/a-b-r-o-w-n/eslint-action?branch=main)

Runs eslint on changed files and creates inline annotations with errors.

## Usage

In `.github/workflows/main.yml`:

```yml
name: Example Workflow

on: [pull_request, push]

jobs:
  lint:
    steps:
      - uses: actions/checkout@v1
      - uses: a-b-r-o-w-n/eslint-action@v2
        with:
          repo-token: "${{ secrets.GITHUB_TOKEN }}"
          files: "src/**/*"
          ignore: "src/some-file-to-ignore.js"
          extensions: ".js,.ts"
          working-directory: "./my-package"
          quiet: "false"
```

# Contributing

Before opening a PR, make sure tests pass and build command is run:

`npm run test && npm run build`
