# cs2-action

Runs and checks if your code is compliant to Epitech's Coding Style

## Usage

A typical GitHub workflow would work like that:

```yaml
on:
  push:

jobs:
  check-coding-style:
    runs-on: ubuntu-latest
    name: Check Coding Style
    steps:
      - uses: actions/checkout@v5
      - uses: hugoschool/cs2-action@v1
```

This runs `cs2` at the root of your repo and reports all the Coding Style errors in a GitHub friendly way.

## Options

- `install_only`: Doesn't run cs2, only installs it for you
- `compile_source`: Compile cs2 from source instead of downloading latest release
- `ref`: Only works with `compile_source` input, specify which ref (commit, branch, tag) to compile from
- `path`: Run cs2 in this directory

Checkout `action.yml` for more information.

Using options is done with the `with` keyword:

```yaml
# ...
steps:
    - uses: actions/checkout@v5
    - uses: hugoschool/cs2-action@v1
      with:
        path: tests/
        install_only: true
```
