# Analytical Platform GitHub Actions

[![Ministry of Justice Repository Compliance Badge](https://github-community.service.justice.gov.uk/repository-standards/api/analytical-platform-github-actions/badge)](https://github-community.service.justice.gov.uk/repository-standards/analytical-platform-github-actions)

[![Open in Dev Container](https://raw.githubusercontent.com/ministryofjustice/.devcontainer/refs/heads/main/contrib/badge.svg)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/ministryofjustice/analytical-platform-github-actions)

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/ministryofjustice/analytical-platform-github-actions)

This repository is a store for Analytical Platform's composite actions and reusable workflows.

## Reusable Workflows

### Container Release

Builds and pushes a container GHCR, including attestations

### Container Scan

Builds and scans a container for vulnerabilities with [Trivy](https://github.com/aquasecurity/trivy) using [aquasecurity/trivy-action](https://github.com/aquasecurity/trivy-action)

### Container Test

Builds and tests a container with [Container Structure Test](https://github.com/GoogleContainerTools/container-structure-test)

### Dependency Review

Runs [actions/dependency-review-action](https://github.com/actions/dependency-review-action)

### Super Linter

Runs [super-linter/super-linter](https://github.com/super-linter/super-linter)

### Zizmor

Runs [woodruffw/zizmor](https://github.com/woodruffw/zizmor)
