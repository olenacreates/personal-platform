# ADR-004: Rendering Strategy

**Status:** Accepted
**Date:** 2026-07-23

## Context

Quality Attribute #1 (Maintainability, interpreted for this project as **Architectural Legibility**) requires an architecture that a technically strong Product Owner working with AI can understand, maintain, and evolve without requiring deep framework expertise.

`PROJECT.md` requires the architecture to support long-term evolution from day one, even though Release 1 implements only a small slice of the eventual product (e.g., Protocol Library, Learning Notes, Case Studies, and possibly richer interactive or CMS-like features later).

Before evaluating specific frameworks, the architecture discussions deliberately evaluated **rendering paradigms** first, since this choice constrains which frameworks are viable and shapes the system's overall complexity.

This decision intentionally precedes framework selection. Rendering strategy is treated as an architectural constraint rather than a consequence of technology choice.

All rendering options considered were technically capable of satisfying current product requirements. The decision was therefore driven by architectural fit rather than technical feasibility.

## Decision

Adopt a **static-first rendering strategy**, with dynamic or server-rendered capability treated as an available but unbuilt future option—not the default architectural posture.

This reflects a reusable engineering principle established during the architecture discussions:

> Preserving optionality is not the same as building capability.

## Alternatives Considered

### Server-side rendering (SSR) as the default

Rejected as the default posture. It introduces operational complexity and a server runtime that the current product does not require.

### Client-side rendering / SPA

Rejected. This project is content-first rather than application-first. A client-rendered architecture would introduce runtime complexity (bundling, hydration, client-side state management) without solving a current product problem.

### Hybrid rendering as the default

Not rejected as an option—only rejected as the default architectural posture. Treating hybrid or dynamic rendering as the starting point would mean paying its complexity cost before any demonstrated need existed.

## Rationale

The primary driver was **Architectural Legibility**.

Static-first is the rendering strategy that a technically strong Product Owner working with AI can most easily understand, maintain, and evolve because it minimizes runtime behavior, operational surface area, and architectural complexity.

The second driver was **proportionality**.

Throughout the architecture discussions, we deliberately avoided solving future problems before they existed. Instead, we chose the smallest architecture that fully satisfies today's confirmed requirements while preserving inexpensive future evolution.

This thinking is captured by the principle:

> Preserving optionality is not the same as building capability.

Performance, hosting simplicity, deployment simplicity, and low operational cost were recognized as valuable consequences of this decision, but they were supporting benefits rather than the primary justification.

## Consequences

### Positive

- The architecture remains legible and low-complexity by default.
- Performance, deployment simplicity, hosting simplicity, and low operational overhead arise naturally from the chosen architecture.
- Future rendering capability can be introduced later if justified, without forcing unnecessary complexity into the MVP.

### Accepted Trade-off

If the platform eventually evolves into something fundamentally application-oriented, additional rendering capability may need to be introduced later.

This trade-off was explicitly accepted because:

- the current product does not require that capability;
- preserving the option is inexpensive;
- implementing it now would increase complexity without delivering current value.

### Explicitly Not Decided

The "escape hatch" is intentionally technology-independent.

The architecture preserves the ability to introduce dynamic rendering in the future if required (for example, search, CMS-like content management, richer interactive features, or selective server-rendered functionality), but deliberately does not prescribe any implementation mechanism at this stage.

Those future capabilities justify preserving the option—they do not justify building the capability today.

## Related Artifacts

- Workshop 01 – Quality Attributes
- ADR-002 – Internationalization Strategy
- ADR-003 – Identity and URL Strategy

## Follow-up Decisions

This rendering strategy establishes an architectural constraint for the subsequent framework evaluation.

The framework selection decision will be documented in a separate Architecture Decision Record.