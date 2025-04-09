# Set Up Crane

This action installs Google's [crane](https://github.com/google/go-containerregistry/tree/main/cmd/crane)

```yaml
jobs:
  container-structure-test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        id: checkout
        uses: actions/checkout@v4

      - name: Set Up crane
        id: setup_crane
        uses: ministryofjustice/analytical-platform-github-actions/setup-crane@main

      - name: Run crane
        id: run_crane
        run: |
          crane ...
```

Specifying a version

```yaml
- name: Set Up crane
  id: setup_crane
  uses: ministryofjustice/analytical-platform-github-actions/setup-crane@main
  with:
    version: v0.20.3
```
