# Contributing Guide

Thank you for helping us improve our projects! This guide explains how to get started, how we work, and which standards keep our repositories healthy.

## Before You Start

1. Review the [Code of Conduct](CODE_OF_CONDUCT.md). We expect everyone to uphold it in all interactions.
2. Read our [Support policy](SUPPORT.md) to understand how we triage issues and feature requests.
3. Familiarize yourself with the [AI operating manual](docs/ai/codex-operating-manual.md) and [.github/copilot instructions](.github/copilot-instructions.md) so automated agents stay aligned with human processes.

## Getting Set Up

- Fork the repository or clone it if you have write access.
- Install dependencies as described in the project `README.md`.
- Create a feature branch (`git checkout -b feature/your-change`). Prefer small, reviewable pull requests (≤ 800 lines changed).

## Development Workflow

1. Make changes with clear, well-tested commits. Update documentation alongside code changes.
2. Run the relevant CI tasks locally (lint, type-check, tests) before opening a PR. Our reusable workflows in [.github/workflow-templates/](.github/workflow-templates/) outline the expected checks.
3. Follow the repository’s coding standards. When in doubt, match the surrounding code.

## Pull Requests

- Use the [pull request template](.github/PULL_REQUEST_TEMPLATE.md) to summarize your changes, rationale, and testing.
- Reference related issues and link to documentation updates.
- Request review from the appropriate owners listed in [CODEOWNERS](CODEOWNERS).
- Keep discussions public when possible so future contributors can learn from the history.

## Issue Management

- Choose the right issue template from [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/) to provide consistent context.
- Label issues accurately so they reach the correct maintainers.
- For security concerns, follow [SECURITY.md](SECURITY.md) instead of opening a public issue.

## Release Cadence

We rely on automation to keep dependencies and release notes current. Refer to [dependabot.yml](dependabot.yml) and [.github/workflow-templates/release-drafter.yml](.github/workflow-templates/release-drafter.yml) for defaults you can adopt in project repositories.

## Questions?

If you are unsure about anything, open a discussion or contact the maintainers as outlined in [SUPPORT.md](SUPPORT.md). We appreciate your contributions!
