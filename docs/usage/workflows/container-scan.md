# Container Scan

Builds and scans a container for vulnerabilities with [Grype](https://github.com/anchore/grype) using [anchore/scan-action](https://github.com/anchore/scan-action)

## Inputs

|         Input          |   Type   | Required |   Default    |
| :--------------------: | :------: | :------: | :----------: |
| `clean-actions-runner` |  `bool`  | `false`  |    `true`    |
|    `container-file`    | `string` | `false`  | `Dockerfile` |

## Usage

```yaml
---
name: 🩻 Container Scan

on:
  pull_request:
    branches:
      - main

permissions: {}

jobs:
  container-scan:
    name: Container Scan
    permissions:
      contents: read
      id-token: write
      pull-requests: write
      security-events: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-container-scan.yml@<commit SHA> # <version>
```
