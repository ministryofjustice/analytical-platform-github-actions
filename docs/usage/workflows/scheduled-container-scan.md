# Scheduled Container Scan

Builds and scans a container for vulnerabilities with [Grype](https://github.com/anchore/grype) using [anchore/scan-action](https://github.com/anchore/scan-action). A Slack alert is sent only when high or critical fixable vulnerabilities are found.

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
