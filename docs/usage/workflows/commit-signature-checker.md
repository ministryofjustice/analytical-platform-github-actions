# Commit Signature Checker

Checks for unverified commits on pull requests

## Usage

```yaml
---
name: ✍️ Commit Signature Checker

on:
  pull_request:
    branches:
      - main

permissions: {}

jobs:
  commit-signature-checker:
    name: Commit Signature Checker
    permissions:
      contents: read
      pull-requests: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-commit-signature-checker.yml@main
```
