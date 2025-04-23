# Chart Lint

Lints a Helm chart with [helm/chart-testing](https://github.com/helm/chart-testing)

## Inputs

|    Input     |   Type   | Required | Default |
| :----------: | :------: | :------: | :-----: |
| `chart-path` | `string` | `false`  | `chart` |

## Usage

```yaml
---
name: 🗺️ Chart Lint

on:
  pull_request:
    branches:
      - main

permissions: {}

jobs:
  chart-lint:
    name: Chart Lint
    permissions:
      contents: read
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-chart-lint.yml@main
```
