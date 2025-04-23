# Container Release

Release a container to GitHub Container Registry, including Cosign and GitHub Attestation

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
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-container-release.yml@main
```
