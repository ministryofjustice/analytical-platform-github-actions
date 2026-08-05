# Dependabot Auto Merge

Automatically approves and merges Dependabot pull requests that update GitHub Actions by a minor version.

## Usage

> [!NOTE]
> You must allow GitHub Actions to create and approve pull requests. Please refer to GitHub's [documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#preventing-github-actions-from-creating-or-approving-pull-requests) for instructions on how to enable this

```yaml
---
name: 🤖 Dependabot Auto Merge

on:
  pull_request:

permissions: {}

jobs:
  dependabot-auto-merge:
    name: Dependabot Auto Merge
    permissions:
      contents: write
      pull-requests: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-dependabot-gh-actions-auto-merge.yml@<commit SHA> # <version>
```
