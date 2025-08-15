# Container Test

Builds and tests a container with [Container Structure Test](https://github.com/GoogleContainerTools/container-structure-test)

## Inputs

|         Input          |  Type  | Required | Default |
| :--------------------: | :----: | :------: | :-----: |
| `clean-actions-runner` | `bool` | `false`  | `true`  |

## Usage

```yaml
---
name: 🧪 Container Test

on:
  pull_request:
    branches:
      - main

permissions: {}

jobs:
  container-test:
    name: Container Test
    permissions:
      contents: read
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-container-test.yml@<commit SHA> # <version>
```
