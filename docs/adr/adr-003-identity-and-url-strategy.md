# ADR-003 — Identity and URL strategy resilient to a future name change

**Status:** Accepted
**Date:** 2026-07-13

## Context

`PROJECT.md` §13 records a hard product constraint: the platform must absorb a likely future surname change (following the Product Owner's divorce) without major restructuring or broken links.

Identity, URLs, route slugs, canonical links, and any name-derived domain or identifiers are established at architecture time. Once content is published and links are shared, a name baked into structure means broken URLs and a migration — exactly what the constraint forbids. The stakes are immediate: `PROJECT.md` §11 has the site being linked from CV, LinkedIn, and job applications, so URL stability matters from the first release. This ADR records the binding constraint and its architectural implications; it does not finalize the domain or brand name, which remains an Architecture Design decision.

## Decision

Keep the person's identity independent of the site's structure, so a name change is a content edit rather than a migration. As facets of that one decision:

1. Do not encode a specific legal name (especially the surname) into URL paths, route slugs, content identifiers, repository/deploy identifiers, or the site's structural identity.
2. Treat the displayed name as editable content/configuration sourced from a single place.
3. Establish stable, name-independent public URLs from the first release; if a name-derived public URL is genuinely unavoidable, back it with a durable redirect so inbound links never break.
4. Require any future domain/brand naming choice to satisfy this constraint; the choice itself is deferred to Architecture Design (and domain purchase to a later cost decision, `PROJECT.md` §9).

## Alternatives considered

- **Surname-based domain and slugs** (e.g. `firstname-surname.tld`, `/surname/...` paths): rejected — a name change would break inbound links and force a migration, directly violating `PROJECT.md` §13.
- **Defer the identity question entirely to implementation:** rejected — public URLs are shared from the first release (`PROJECT.md` §11); recording the constraint now prevents an early, hard-to-reverse mistake, even though the concrete naming is deferred.

## Consequences

- A future name change becomes a small content/configuration edit; inbound links from CV/LinkedIn/applications stay valid; canonical URLs and SEO are protected.
- Trade-off: rules out vanity surname-based slugs or domains, and asks the architecture to treat the display name as data from the outset.

## Impacted Artifacts

- `PROJECT.md` §13 (the constraint), §11 (inbound links), §9 (deferred domain/cost) — this ADR operationalizes the §13 constraint.
- [ADR-002](adr-002-i18n-strategy.md) — locale URL design must stay compatible with name-independent URLs.
- `CLAUDE.md` — carries this as a binding constraint for work in the repository.
- Architecture Design documents — must choose the domain, brand, and URL structure within this constraint, and may record a follow-up ADR when the domain is chosen.
