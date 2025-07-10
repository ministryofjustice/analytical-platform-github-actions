# OpenSSF Scorecard

Runs [ossf/scorecard-action](https://github.com/ossf/scorecard-action)

## Usage

```yaml
---
name: 🛡️ OpenSSF Scorecard

on:
  push:
    branches:
      - main
  schedule:
    - cron: "30 6 * * 1"

permissions: {}

jobs:
  openssf-scorecard:
    name: OpenSSF Scorecard
    permissions:
      contents: read
      id-token: write
      security-events: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-openssf-scorecard.yml@<commit SHA> # <version>
```
