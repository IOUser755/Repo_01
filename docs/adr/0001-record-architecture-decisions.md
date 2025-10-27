# ADR 0001: Record architecture decisions

- Status: Accepted
- Deciders: AP2_01 bootstrap maintainers
- Date: 2024-04-01

## Context

The AP2_01 project will evolve quickly as we refine the MERN stack, integrate Tailwind, and connect to MongoDB Atlas. Without a shared log of architectural decisions, future contributors would lose the rationale behind critical choices.

## Decision

We will track Architecture Decision Records (ADRs) in `docs/adr/` using the shared template (`docs/adr/TEMPLATE.md`). Each record receives a monotonically increasing identifier and ships alongside the change that implements the decision.

## Consequences

- ✅ Preserves architectural intent for anyone onboarding to the project.
- ✅ Creates a lightweight review artifact for major technical pivots.
- ⚠️ Requires discipline to document decisions as they occur.
- ❌ Introduces a minor amount of overhead when proposing changes, which we accept for the long-term clarity it provides.
