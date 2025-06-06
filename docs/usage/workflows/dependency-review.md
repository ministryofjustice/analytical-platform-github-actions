# Dependency Review

Runs [actions/dependency-review-action](https://github.com/actions/dependency-review-action)

## Usage

> [!NOTE]
> This workflow only works with public repositories

```yaml
---
name: 🔍 Dependency Review

on:
  pull_request:
    branches:
      - main

permissions: {}

jobs:
  dependency-review:
    name: Dependency Review
    permissions:
      contents: read
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-dependency-review.yml@<commit SHA> # <version>
```
