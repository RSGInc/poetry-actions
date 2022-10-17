# poetry-actions

GitHub action for installing `poetry` dependencies into a Python environment.

## Usage

### Install Specific Group

```yaml
name: CI

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Install Lint Dependencies
        uses: RSGInc/poetry-actions
        with:
          python_version: 3.9
          group: lint
```

### Install All Poetry Dependencies

```yaml
name: CI

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Install Python Dependencies
        uses: RSGInc/poetry-actions
        with:
          python_version: 3.9
```
