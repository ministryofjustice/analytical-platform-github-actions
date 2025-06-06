# Scheduled Container Scan

Scans the latest release for vulnerabilities with [Trivy](https://github.com/aquasecurity/trivy) using [aquasecurity/trivy-action](https://github.com/aquasecurity/trivy-action)

## Inputs

|      Input      |   Type   | Required |     Default     |
| :-------------: | :------: | :------: | :-------------: |
| `scan-severity` | `string` | `false`  | `HIGH,CRITICAL` |

## Usage

```yaml
---
name: ⏰ Scheduled Container Scan

on:
  schedule:
    - cron: "0 9 * * 1-5" # Every weekday at 9AM UTC
  workflow_dispatch:

permissions: {}

jobs:
  scheduled-container-scan:
    name: Scheduled Container Scan
    permissions:
      contents: read
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-scheduled-container-scan.yml@<commit SHA> # <version>
    secrets:
      cve-scan-slack-webhook-url: ${{ secrets.ANALYTICAL_PLATFORM_CVE_SCAN_SLACK_WEBHOOK_URL }}
```
