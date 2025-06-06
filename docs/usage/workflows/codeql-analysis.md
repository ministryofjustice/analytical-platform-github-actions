# CodeQL Analysis

Runs [github/codeql-action/analyze](https://github.com/github/codeql-action/tree/main/analyze)

## Inputs

|    Input    |   Type   | Required |     Default     |
| :---------: | :------: | :------: | :-------------: |
| `languages` | `string` | `false`  | `'["actions"]'` |

## Usage

```yaml
---
name: 🔬 CodeQL Analysis

on:
  pull_request:
    branches:
      - main
  push:
    branches:
      - main

permissions: {}

jobs:
  codeql-analysis:
    name: CodeQL Analysis
    permissions:
      contents: read
      security-events: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-codeql-analysis.yml@<commit SHA> # <version>
```

### Including Languages

> [!NOTE]
> You must include `actions`

```yaml
---
jobs:
  codeql-analysis:
    name: CodeQL Analysis
    permissions:
      contents: read
      security-events: write
    uses: ministryofjustice/analytical-platform-github-actions/.github/workflows/reusable-codeql-analysis.yml@<commit SHA> # <version>
    with:
      languages: '["actions", "python"]'
```
