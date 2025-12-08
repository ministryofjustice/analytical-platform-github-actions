# Container Release

Release a container to GitHub Container Registry, including Cosign and GitHub Attestation

## Inputs

|         Input          |   Type   | Required |   Default    |
| :--------------------: | :------: | :------: | :----------: |
| `clean-actions-runner` |  `bool`  | `false`  |    `true`    |
|    `container-file`    | `string` | `false`  | `Dockerfile` |

## Usage

```yaml
---
name: 🔖 Container Release

on:
  push:
    tags:
      - "*"

permissions: {}

jobs:
  container-release:
    name: Container Release
    permissions:
      actions: read
      attestations: write
      contents: write
      id-token: write
      packages: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-container-release.yml@<commit SHA> # <version>
    secrets:
           analytical-platform-container-test-slack-webhook-url: ${{ secrets.ANALYTICAL_PLATFORM_CONTAINER_TEST_SLACK_WEBHOOK_URL }}
```
