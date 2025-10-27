# AP2_01

AP2_01 bootstraps a MongoDB, Express, React, and Node.js (MERN) application using the organization foundation repo as its baseline. The project reuses the shared automation, documentation, and governance playbooks so contributors can focus on shipping product value quickly.

## Project overview

- **Stack**: React front end with Tailwind CSS, Express/Node.js API, and MongoDB Atlas.
- **Status**: Fresh scaffold copied from the [`template-mern`](https://github.com/IOUser755/template-mern) starter.
- **Governance**: Aligns with the organization-wide defaults published in the [foundation repo](https://github.com/IOUser755/Repo_01).

## Getting started

1. Install the Node.js version defined in `.nvmrc` (see the template repository) and run `npm install` in both `client/` and `server/` directories.
2. Copy `.env.example` to `.env` for each workspace and fill in service URLs, MongoDB connection strings, and API secrets.
3. Start local services:
   - `npm run dev` inside `client/` to launch Vite + Tailwind.
   - `npm run dev` inside `server/` to run the Express API with hot reload.
4. Run `npm run lint`, `npm run test`, and `npm run typecheck` in each workspace before submitting pull requests.

## Documentation

- Architecture notes live in [ARCHITECTURE.md](ARCHITECTURE.md).
- Contribution guidance is captured in [CONTRIBUTING.md](CONTRIBUTING.md).
- Architecture Decision Records (ADRs) reside in [`docs/adr/`](docs/adr/) using the shared template.
- Agent playbooks, Codex prompts, and automation checklists are available under [`docs/ai/`](docs/ai/).

## Automation

- Continuous integration is configured via [`.github/workflows/ci.yml`](.github/workflows/ci.yml) and automatically detects Node.js projects.
- Dependency updates arrive weekly through [`.github/dependabot.yml`](.github/dependabot.yml).

### Follow-ups

- [ ] Enable branch protection on `main`.
- [ ] Map placeholders in `.github/CODEOWNERS` to real teams.
- [ ] Provision dev, staging, and production environments.
