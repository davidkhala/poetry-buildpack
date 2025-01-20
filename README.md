# davidkhala/poetry-builpack

## Use

```
steps:
- uses: actions/checkout@main
- uses: davidkhala/poetry-buildpack@main
  with:
    working-directory: . # directory path (dirname) of file `pyproject.toml`. Default to current directory
    test-entry-point: echo 'test' # testing entry-point commands. such as `pytest`. If not specified, testing step will be skipped
    tests: tests # testing sources root directory.  Default `tests`
    version: 3.12 # python version. If not specified, default to runner's python version
    extras: extra1 extra2 # extras to be installed. It should be subset of extras defined in Default to install all extras
```

## Design
`shell: bash` is a alignment to `snok/install-poetry`
