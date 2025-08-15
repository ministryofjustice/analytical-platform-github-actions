# Container Scan

Builds and scans a container for vulnerabilities with [Trivy](https://github.com/aquasecurity/trivy) using [aquasecurity/trivy-action](https://github.com/aquasecurity/trivy-action)

## Inputs

|         Input          |   Type   | Required |     Default     |
| :--------------------: | :------: | :------: | :-------------: |
| `clean-actions-runner` |  `bool`  | `false`  |     `true`      |
|    `scan-severity`     | `string` | `false`  | `HIGH,CRITICAL` |

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
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-container-scan.yml@<commit SHA> # <version>
```
