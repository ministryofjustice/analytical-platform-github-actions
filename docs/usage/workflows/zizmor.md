# Zizmor

Runs [woodruffw/zizmor](https://github.com/woodruffw/zizmor)

## Usage

```yaml
---
name: 🌈 Zizmor

on:
  pull_request:
    branches:
      - main

permissions: {}

jobs:
  zizmor:
    name: Zizmor
    permissions:
      actions: read
      contents: read
      security-events: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-zizmor.yml@main
```
