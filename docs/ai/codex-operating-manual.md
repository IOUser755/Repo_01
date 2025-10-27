# Codex Operating Manual

This manual documents how automated assistants participate in this organization. Share it widely and link it from related docs so humans and AI collaborators follow the same expectations.

## Core Principles

- Prefer small, reviewable pull requests (≤ 800 changed lines) that include rationale, testing, and rollback guidance.
- Cross-link every new document or workflow so future contributors can rediscover it quickly.
- Never store or output secrets. Use placeholders and least-privilege tokens instead.
- Automate checks through reusable workflows whenever possible, falling back to manual validation if tooling is unavailable.

## Collaboration Workflow

1. **Understand scope**: Read repository-specific `AGENTS.md` files, [CONTRIBUTING.md](../../CONTRIBUTING.md), and [.github/copilot-instructions.md](../../.github/copilot-instructions.md) before making changes.
2. **Plan first**: Outline changes, confirm constraints, and ask clarifying questions when requirements are ambiguous.
3. **Implement carefully**: Follow coding standards, update documentation, and add tests or workflows to keep quality high.
4. **Document outputs**: Every PR must summarize changes, note testing status, mention risks, and list follow-ups.
5. **Handover**: After merging, update any relevant docs, dashboards, or issue trackers so humans know what changed.

## Communication Norms

- Use inclusive, professional language in commits, PRs, and issue comments.
- Escalate blockers quickly; do not silently drop tasks when access is missing.
- Reference canonical docs (this manual, [CONTRIBUTING.md](../../CONTRIBUTING.md), [SUPPORT.md](../../SUPPORT.md)) when guiding humans.

## Environment & Access Constraints

- Confirm whether the execution environment has outbound network access before attempting to push branches or contact external services.
- When the environment cannot reach GitHub remotes (for example, HTTP 403 from a proxy), document the failure in the PR and provide copy-pasteable commands that a human can run locally.
- Never attempt to bypass organizational security controls. Instead, notify maintainers using the contacts listed in [SUPPORT.md](../../SUPPORT.md) so they can perform the privileged action.

## Compliance Checklist

Before finishing work, automated contributors must confirm:

- [ ] Changes are committed on the correct branch and a PR is ready with all required sections.
- [ ] Related docs reference each other for discoverability.
- [ ] Sensitive data was never introduced.
- [ ] Tests or validations ran when feasible; otherwise note limitations in the PR.

Keep this manual updated as processes evolve. Link revisions from release notes or change logs so teams can trace history.
