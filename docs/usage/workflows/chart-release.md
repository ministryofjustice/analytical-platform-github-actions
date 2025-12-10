# Chart Release

Releases a Helm Chart to GitHub Container Registry, including Cosign and GitHub Attestation

## Inputs

|    Input     |   Type   | Required | Default |
| :----------: | :------: | :------: | :-----: |
| `chart-name` | `string` |  `true`  |         |
| `chart-path` | `string` | `false`  | `chart` |

## Usage

```yaml
---
name: 🔖 Chart Release

on:
  push:
    tags:
      - "*"

permissions: {}

jobs:
  chart-release:
    name: Chart Release
    permissions:
      actions: read
      attestations: write
      contents: write
      id-token: write
      packages: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-chart-release.yml@<commit SHA> # <version>
    secrets:
      release-failure-webhook-url: ${{ secrets.ANALYTICAL_PLATFORM_RELEASE_FAILURE_SLACK_WEBHOOK_URL }}
    with:
      chart-name: example-chart-name
```
