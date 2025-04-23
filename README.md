# Analytical Platform GitHub Actions

[![Ministry of Justice Repository Compliance Badge](https://github-community.service.justice.gov.uk/repository-standards/api/analytical-platform-github-actions/badge)](https://github-community.service.justice.gov.uk/repository-standards/analytical-platform-github-actions)

[![Open in Dev Container](https://raw.githubusercontent.com/ministryofjustice/.devcontainer/refs/heads/main/contrib/badge.svg)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/ministryofjustice/analytical-platform-github-actions)

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/ministryofjustice/analytical-platform-github-actions)

This repository is a store for Analytical Platform's composite actions and reusable workflows.

---

## Composite Actions

### Clean Actions Runner

See [`clean-actions-runner`](/clean-actions-runner/README.md)

### Set Up Container Structure Test

See [`setup-container-structure-test`](/setup-container-structure-test/README.md)

### Set Up Crane

See [`setup-crane`](/setup-crane/README.md)

---

## Reusable Workflows

### Chart Lint

Lints a Helm chart with [helm/chart-testing](https://github.com/helm/chart-testing)

### Chart Release

Pushes a chart to GHCR

### CodeQL Analysis

Runs [github/codeql-action/analyze](https://github.com/github/codeql-action/tree/main/analyze)

### Container Release

Builds and pushes a container GHCR, including attestations

### Container Scan

Builds and scans a container for vulnerabilities with [Trivy](https://github.com/aquasecurity/trivy) using [aquasecurity/trivy-action](https://github.com/aquasecurity/trivy-action)

### Container Test

Builds and tests a container with [Container Structure Test](https://github.com/GoogleContainerTools/container-structure-test)

### Dependency Review

Runs [actions/dependency-review-action](https://github.com/actions/dependency-review-action)

### Scheduled Container Scan

Pulls latest release of a container and scans for vulnerabilities with [Trivy](https://github.com/aquasecurity/trivy) using [aquasecurity/trivy-action](https://github.com/aquasecurity/trivy-action)

### Super Linter

Runs [super-linter/super-linter](https://github.com/super-linter/super-linter)

### Zizmor

Runs [woodruffw/zizmor](https://github.com/woodruffw/zizmor)
