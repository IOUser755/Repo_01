# Copilot & AI Assistant Instructions

These guidelines keep AI pair programmers aligned with our processes. Share them in repositories where automated assistance is enabled.

## General Expectations

- Follow the [Codex operating manual](../docs/ai/codex-operating-manual.md) for overarching policies.
- Default to small, incremental changes with thorough commit messages and PR descriptions.
- Reference relevant docs (README, CONTRIBUTING, SUPPORT) in suggestions so humans can validate the approach.
- Never invent or expose secrets, credentials, or private data. Use placeholders such as `TOKEN_GOES_HERE` when examples are required.

## Working on Pull Requests

- Respect the [pull request template](PULL_REQUEST_TEMPLATE.md) sections and populate each one.
- Call out testing steps even when they are skipped due to tooling limits.
- Link to new or updated documentation so reviewers can cross-check instructions.

## Coding Style

- Follow existing conventions; if unsure, mirror surrounding code and note open questions in the PR.
- Prefer explicit names, clear logging, and graceful error handling without leaking sensitive information.
- Keep configuration files deterministic and comments informative but concise.

## Communication

- Ask for clarification when requirements conflict or context is missing.
- Summarize reasoning in commit messages and PR bodies so reviewers understand trade-offs.
- Flag risks or manual follow-ups, especially when automation is intentionally limited.

Refer back to this document whenever onboarding a new repository or assistant. Update it in tandem with [CONTRIBUTING.md](../CONTRIBUTING.md) to keep instructions consistent.
