# Repo_01

This repository hosts shared GitHub defaults for the organization. Review the governance docs and automation templates below before onboarding a new project.

## Organization policies

- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Security policy](SECURITY.md)
- [Support policy](SUPPORT.md)
- [Contributing guide](CONTRIBUTING.md)
- [AI operating manual](docs/ai/codex-operating-manual.md)
- [Copilot & AI instructions](.github/copilot-instructions.md)

All documents are cross-linked so humans and automated contributors can rediscover them quickly.

## Workflow templates

Reusable workflow templates live under [`.github/workflow-templates/`](.github/workflow-templates/):

- [`node-ci.yml`](.github/workflow-templates/node-ci.yml) – Node.js linting and tests when a `package.json` is present.
- [`python-ci.yml`](.github/workflow-templates/python-ci.yml) – Python linting and testing with Ruff, Flake8, and Pytest when available.
- [`go-ci.yml`](.github/workflow-templates/go-ci.yml) – Go vet and test jobs for Go modules.
- [`generic-ci.yml`](.github/workflow-templates/generic-ci.yml) – No-op workflow that documents detected languages.
- [`codeql-analysis.yml`](.github/workflow-templates/codeql-analysis.yml) – CodeQL scans for JavaScript/TypeScript, Python, and Go.
- [`dependency-review.yml`](.github/workflow-templates/dependency-review.yml) – Dependency review checks on pull requests.
- [`release-drafter.yml`](.github/workflow-templates/release-drafter.yml) – Release Drafter automation; pair with the release config below.

## Release automation

Release note defaults live in [`.github/release-drafter.yml`](.github/release-drafter.yml). Dependabot defaults live in [`.github/dependabot.yml`](.github/dependabot.yml) and the org-level [dependabot.yml](dependabot.yml).

## Pushing these templates to GitHub

Use the commands below to publish the branch that contains these assets. Choose the path that matches the repository you are targeting.

### Push to this repository (`Repo_01`)

```bash
# Initialize if you cloned without history
git init
git add .
git commit -m "Initial commit"

# Ensure the main branch exists locally
git branch -M main

# Point to the Repo_01 remote (use SSH if you prefer)
git remote add origin https://github.com/IOUser755/Repo_01.git

# Confirm the remote URL
git remote -v

# Publish the default branch
git push -u origin main

# Optional: publish the feature branch that carries these templates
git checkout -b work
git push -u origin work
```

### Push to an organization-level `.github` repository

```bash
git clone https://github.com/<org>/.github.git
cd .github

# Copy or create the templates in workflow-templates/
mkdir -p workflow-templates

# Stage, commit, and push the updates
git add .
git commit -m "Add workflow templates and defaults"
git push
```

### Adjust an existing remote

If the remote already exists but points elsewhere, update it instead of adding a new one:

```bash
git remote set-url origin https://github.com/IOUser755/Repo_01.git
```

You can also keep multiple remotes (for example, `origin` for `Repo_01` and `upstream` for the org-level `.github` repository) if you need to push to both locations.

## Organization security settings to enable

After these templates are merged, ensure the following GitHub organization settings are toggled on so the automation can enforce policy:

- Dependabot alerts and automated security updates
- Secret scanning with push protection
- Dependency review for pull requests
- Default CodeQL code scanning for eligible repositories
- Branch protection or rulesets that require lint, typecheck, and test workflows to pass
