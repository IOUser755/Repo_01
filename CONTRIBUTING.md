# Contributing to AP2_01

Thanks for investing time in AP2_01. This document captures the minimum workflow required to keep the MERN stack healthy while the project is in its bootstrap phase. For expanded governance policies, reference the shared [foundation repo](https://github.com/IOUser755/Repo_01).

## Development workflow

1. Create a feature branch from `main` using a descriptive name (e.g., `feature/auth-api`).
2. Keep pull requests focused and under 400 changed lines whenever possible.
3. Ensure commits are signed or otherwise attributable per organization policy.

## Required checks

Run the following scripts locally before pushing:

- `npm run lint` in both `client/` and `server/`
- `npm run test` in both workspaces
- `npm run typecheck` in both workspaces (or `tsc --noEmit` if available)

The CI workflow mirrors these commands. Fix issues locally before requesting review to keep the pipeline green.

## Documentation and ADRs

- Update [ARCHITECTURE.md](ARCHITECTURE.md) when altering system boundaries or integration patterns.
- Capture significant technical decisions in [`docs/adr/`](docs/adr/) using the provided template.
- Agent playbooks live under [`docs/ai/`](docs/ai/); refresh them when workflows change so AI collaborators stay aligned.

## Pull request expectations

- Fill out the PR template completely, including risk assessment and test evidence.
- Request reviews from the appropriate owners listed in `.github/CODEOWNERS` once those mappings are finalized.
- Use draft pull requests for work-in-progress changes to avoid premature reviews.

## Community conduct

This project follows the organization's [Code of Conduct](CODE_OF_CONDUCT.md). Report incidents through the established internal channels.
