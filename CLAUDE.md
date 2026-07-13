# CLAUDE.md — Repository Operating Guide

Operating guide for anyone (human or AI) working in this repository. Keep it short; when in doubt, defer to the linked sources of truth.

## What this repository is

An experiment in **designing an AI Engineering Workflow**. The workflow is the primary outcome; this website is **Case Study #1** (see [ADR-001](docs/adr/adr-001.md)). The product itself is a personal professional platform.

**Product source of truth:** [`PROJECT.md`](PROJECT.md). Read it before making product or scope decisions — especially §6 (MVP scope) and §7 (explicitly deferred).

## Current phase

**Entering Architecture Design.** Product Discovery is complete and confirmed (see [`docs/discovery/product-discovery-report.md`](docs/discovery/product-discovery-report.md)). Work proceeds through the SDLC protocols in [`protocols/`](protocols/).

## Sources of truth — read these first

| To understand… | Read |
|---|---|
| What we're building and what's out of scope | [`PROJECT.md`](PROJECT.md) |
| Decisions already made | [`docs/adr/`](docs/adr/) |
| How we work | [`docs/core-principles/engineering-principles.md`](docs/core-principles/engineering-principles.md) |
| Why the product is shaped this way | [`docs/discovery/product-discovery-report.md`](docs/discovery/product-discovery-report.md) |

## Non-negotiables when working here

- **Priority order when constraints conflict:** quality > architecture > date. **Cut scope before quality or architecture** (`PROJECT.md` §9).
- **Authenticity:** publish only work you can stand behind; label unfinished work openly as *work in progress*; never fake completeness.
- **Respect scope:** build within `PROJECT.md` §6. Do not pull deferred §7 capabilities into the MVP.
- **Evolvability without over-engineering:** *build the smallest implementation that preserves the long-term architecture.* Design clean seams, don't pre-build deferred features.
- **Honor the binding constraints:** English-first but i18n-ready ([ADR-002](docs/adr/adr-002-i18n-strategy.md)); name-independent identity and URLs ([ADR-003](docs/adr/adr-003-identity-and-url-strategy.md)).

## Recording decisions

Record decisions as ADRs in [`docs/adr/`](docs/adr/), using: **Status · Context · Decision · Consequences**. *Capture decisions, not conversations.* Don't let load-bearing decisions live only in prose or in chat — if the architecture will lean on it, it needs an ADR.

## Working agreement (human + AI)

- **Human = Product Owner** (vision, priorities, approvals). **AI = engineering collaborator.**
- Don't propose implementation, technology, or code until the phase warrants it and the relevant decision is made. When unsure, surface options and trade-offs rather than assuming.
- Distinguish **project standards** from **general best practice** — label the latter, so it's never mistaken for a decision the owner made.
- Every SDLC phase produces explicit artifacts. Every PR documents not just code but the decisions, scope boundaries, and next handoff (see [`.github/pull_request_template.md`](.github/pull_request_template.md)).

## Git workflow

- One feature branch per unit of work; open a PR using the template; merge to `main`.
- Infrastructure is **free-first** for the MVP (`PROJECT.md` §9); paid services are a later, deliberate investment.
