# Octo STS

This action clones private repositories using [Octo STS](https://github.com/apps/octo-sts)

## Inputs

| Input                    | Type     | Required | Default                                     |
| ------------------------ | -------- | -------- | ------------------------------------------- |
| `octo-sts-configuration` | `string` | false    | `.github/analytical-platform/octo-sts.json` |
| `octo-sts-domain`        | `string` | false    | `octo-sts.dev`                              |
| `temporary-token-file`   | `string` | false    | `/tmp/octo-sts-token`                       |

## Usage

```yaml
jobs:
  octo-sts:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      id-token: write # Required permission for enable OIDC
    steps:
      - name: Octo STS
        id: octo_sts
        uses: ministryofjustice/analytical-platform-github-actions/octo-sts@<commit SHA> # <version>
```

## Octo STS Configuration File

```jsonc
[
  {
    "scope": "<GitHub organisation>/<GitHub repository>", // Source repository to clone e.g. ministryofjustice/private-repository
    "identity": "<STS identity>", // STS identity e.g. ministryofjustice-example-repository
    "branch": "<branch or tag>", // Branch or tag of source repository to checkout when cloning
  },
]
```
