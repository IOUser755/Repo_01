# AP2_01 Architecture

AP2_01 is a MERN monorepo that pairs a React client with a Node.js API. The layout mirrors the organization foundation repo so shared automation, documentation, and AI assistants function without modification.

## Module map

```
/               Project governance, automation, and bootstrap documentation
/client/        React + Vite frontend with Tailwind CSS
/server/        Express API with MongoDB data access layer
/docs/          ADRs, AI agent playbooks, and onboarding checklists
```

## Data flow

1. The React client communicates with the Express API over HTTPS using JSON payloads.
2. The API persists and queries documents in MongoDB (Atlas by default) through an ODM such as Mongoose.
3. Authentication will be handled with JWT-based sessions once the auth module is scaffolded.

## Operational tooling

- Continuous integration: GitHub Actions via [`.github/workflows/ci.yml`](.github/workflows/ci.yml).
- Dependency management: Dependabot configured in [`.github/dependabot.yml`](.github/dependabot.yml).
- Observability, logging, and infrastructure provisioning will reuse the patterns documented in the [foundation repo](https://github.com/IOUser755/Repo_01) until project-specific tooling is selected.

## Decision records

Architecture Decision Records (ADRs) live in [`docs/adr/`](docs/adr/). Start with `0001-record-architecture-decisions.md` and create new entries as the system evolves.
