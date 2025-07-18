# Set Up Container Structure Test

This action installs Google's [Container Structure Test](https://github.com/GoogleContainerTools/container-structure-test)

> [!WARNING]
> Container Structure Test is not an officially supported Google project, and is currently in maintainence mode.
> However, releases are still being created.

## Inputs

| Input          | Type     | Required | Default               |
| -------------- | -------- | -------- | --------------------- |
| `github-token` | `string` | false    | `${{ github.token }}` |
| `version`      | `string` | false    | `latest`              |

## Usage

> [!WARNING]
> This action only works with versions of Container Structure Test that are released to GitHub.
> v1.17.0 onwards.

```yaml
- name: Set Up Container Structure Test
  id: setup_container_structure_test
  uses: ministryofjustice/analytical-platform-github-actions/setup-container-structure-test@<commit SHA> # <version>

- name: Run Container Structure Test
  id: run_container_structure_test
  run: |
    container-structure-test ...
```

Specifying a version

```yaml
- name: Set Up Container Structure Test
  id: setup_container_structure_test
  uses: ministryofjustice/analytical-platform-github-actions/setup-container-structure-test@<commit SHA> # <version>
  with:
    version: v1.17.0
```
