# ADR-002 — Internationalization (i18n) strategy

**Status:** Accepted
**Date:** 2026-07-13

## Context

`PROJECT.md` §10 records the product decision that English is the primary language, with German and Ukrainian planned as supported languages in future iterations. §4 requires the architecture to support the platform's long-term evolution from day one, while §6 keeps the MVP intentionally small.

Localization is a cross-cutting concern that shapes URL structure, routing, and the content model. Retrofitting it onto a site built single-language is expensive and typically breaks existing URLs — the rework the "evolvable from day one" principle exists to prevent. The architect therefore needs a clear i18n *stance* before making those foundational choices. This ADR sets that stance; it does not choose an i18n mechanism, which is Architecture Design work.

## Decision

Ship the MVP in English only, and architect the platform to be **i18n-ready** rather than multilingual. As facets of that one decision:

1. No translated content, locale switching, or translation tooling in the first release.
2. Design the URL/routing scheme and content model so a locale dimension can be added later without restructuring or breaking existing English URLs, keeping user-facing content separable from layout and logic.
3. "i18n-ready" means keeping the seam for a future locale clean — not building a translation system now, which would violate the small-MVP and anti-over-engineering principles.
4. Defer the i18n mechanism (framework capability, library, routing pattern) to Architecture Design, to be recorded in its own ADR when chosen.

## Alternatives considered

- **Build a multilingual MVP now (English + German + Ukrainian):** rejected — violates the intentionally-small MVP scope and the tight timeline, with no validated need yet; contradicts "invest after validation."
- **Single-language MVP with no i18n consideration, retrofit later:** rejected — retrofitting i18n typically breaks URLs and forces restructuring, directly violating the evolvability-from-day-one requirement (`PROJECT.md` §4).
- **Choose the i18n mechanism now:** rejected — the mechanism is a design decision; settling it before Architecture Design would be premature and out of phase.

## Consequences

- Adding German and Ukrainian later becomes an incremental change rather than a migration, and the English URLs shared from CV/LinkedIn stay stable.
- Trade-off: a small amount of upfront design attention is spent keeping the locale seam clean for a capability the MVP won't use. A strict reading could tempt over-engineering; that is held in check by the principle "build the smallest implementation that preserves the long-term architecture."

## Impacted Artifacts

- `PROJECT.md` §4, §10 — this ADR operationalizes the localization intent recorded there.
- [ADR-003](adr-003-identity-and-url-strategy.md) — the URL strategy must remain compatible with a future locale segment.
- `CLAUDE.md` — carries this as a binding constraint for work in the repository.
- Architecture Design documents — must adopt an i18n-ready URL/routing scheme and content model, and record the chosen mechanism in a follow-up ADR.
