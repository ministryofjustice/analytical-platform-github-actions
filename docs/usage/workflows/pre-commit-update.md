# pre-commit Update

Updates pre-commit hook versions

##

> [!NOTE]
> You must allow GitHub Actions to create and approve pull requests. Please refer to GitHub's [documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#preventing-github-actions-from-creating-or-approving-pull-requests) for instructions on how to enable this

```yaml
---
name: 🅿️ pre-commit Update

on:
  schedule:
    - cron: "0 9 * * 1-5" # Monday-Friday at 09:00 UTC
  workflow_dispatch:

permissions: {}

jobs:
  pre-commit-update:
    name: pre-commit Update
    permissions:
      contents: write
      pull-requests: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-pre-commit-update.yml@<commit SHA> # <version>
```
