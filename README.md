# Pyre Check
GitHub Action to check Python Repositories against [Pyre](https://github.com/facebook/pyre-check)

## Example Workflow

```
name: Static Analysis against Pyre

on: pull_request

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.x
      uses: actions/setup-python@v1
      with:
        python-version: '3.x'
    - name: Pyre-Check Action Step
      uses: ./
      with:
        token: ${{ secrets.GITHUB_TOKEN }}
```

### Sources
Took example of how to use GitHub Actions to comment on PRs from https://github.com/yokawasa/action-sqlcheck.
