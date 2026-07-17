# Shared GitHub Workflows

Reusable GitHub Actions workflows for Connor Fuglestad's Python, data science, and web projects.

## Available workflows

### Python CI

```yaml
jobs:
  ci:
    uses: cfuglestad/github-workflows/.github/workflows/python-ci.yml@main
    with:
      python-version: "3.12"
      coverage-threshold: 80
```

The workflow installs the project with its `dev` extras, then runs Ruff, Black, MyPy, Pytest, and coverage.

### Node / Astro CI

```yaml
jobs:
  ci:
    uses: cfuglestad/github-workflows/.github/workflows/node-ci.yml@main
    with:
      node-version: "22"
```

The workflow installs dependencies, runs available format and lint scripts, and creates a production build.

## Versioning

Templates reference `@main` initially so improvements flow through automatically. Mature repositories should pin a release tag such as `@v1` for stronger reproducibility.

## Security

Workflows use read-only repository permissions by default and pin official actions to stable major versions. No secrets are required for standard CI.
