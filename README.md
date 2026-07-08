# cs2-action

Runs and checks if your code is compliant to Epitech's Coding Style

> [!NOTE]
> If you're an Epitech student and you wish to use this action, I highly recommand creating a repository on your personal account that mirrors to the Epitech repo.
>
> Epitech's repos can make it hard to use external actions. Using your own repos allow total control over your CI.

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
      - uses: actions/checkout@v7
      - uses: hugoschool/cs2-action@v1
```

This runs `cs2` at the root of your repo and reports all the Coding Style errors in a GitHub friendly way.

## Options

- `install_only`: Doesn't run cs2, only installs it for you
- `compile_source`: Compile cs2 from source instead of downloading latest release
- `ref`: Only works with `compile_source` input, specify which ref (commit, branch, tag) to compile from
- `path`: Run cs2 in this directory
- `options`: Run cs2 with these options (example: `-j2`)

Checkout `action.yml` for more information.

Using options is done with the `with` keyword:

```yaml
# ...
steps:
    - uses: actions/checkout@v7
    - uses: hugoschool/cs2-action@v1
      with:
        path: tests/
        install_only: true
```
