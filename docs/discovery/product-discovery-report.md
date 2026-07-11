# Product Discovery Report

**Project:** Personal Platform (an experiment in Designing an AI Engineering Workflow)
**Protocol:** 01 — Project Discovery (v1.0)
**SDLC phase:** Product Discovery
**Product Owner:** Olena Lendiel
**Facilitator:** AI (Product Discovery Facilitator)
**Date completed:** 2026-07-11
**Status:** ✅ Complete — confirmed by the Product Owner

---

## 1. Purpose of this report

This report documents *how* shared understanding of the product was reached during Product Discovery — the questions explored, the reasoning, the tensions surfaced, and how each was resolved. It is the audit trail behind [`PROJECT.md`](../../PROJECT.md).

`PROJECT.md` is the canonical, forward-looking product definition. This report is the record of the discovery journey that produced it.

---

## 2. Inputs discovered in the repository

Before the interview, the following existing artifacts were inspected and treated as hypotheses until confirmed:

- `README.md` — "Personal platform showcasing projects, engineering thinking, and AI-assisted software development."
- `protocols/01-project-discovery.md` — the discovery protocol itself (v1.0).
- `docs/adr/adr-001.md` — **ADR-001:** "The workflow is the primary outcome. The website is one artifact produced during the experiment."

ADR-001 was treated as an **established constraint** and was not reopened.

---

## 3. Discovery journey — topics and resolutions

### 3.1 Why the project exists
Explored the underlying motivation. Established that the driver is **not productivity or faster code**, but a deeper question: how AI changes the way engineers think, collaborate, learn, and decide.

Refined by the Product Owner into a single system:
- **Goal:** design and validate an AI Engineering Workflow.
- **Approach:** systems thinking + learning through building.
- **Primary deliverable:** reusable knowledge.
- **Impact:** sharing with the community.

Key nuance: the target is **knowledge reusable by others**, not learning for its own sake — a distinction that governs documentation and success evaluation. The project is also a practical validation of the Product Owner's Career Engineering Framework.

### 3.2 Target audience
Narrowed from "the community" to a specific group: **domain experts learning to collaborate with AI intentionally** — people transitioning into technical roles and technical-adjacent professionals (QA, TPM, BA, PM, Scrum Masters, engineering managers). Unified by *need*, not title. The MVP's audience is distinct: hiring managers, recruiters, collaborators, conference organizers.

### 3.3 Tension: software workflow vs. non-developer audience — *resolved*
**Raised:** the workflow is validated by building software, yet the audience is largely non-developers — risking engineering-specific assumptions that don't transfer.

**Resolution:** the platform is **Case Study #1**, not final proof. Software was chosen *deliberately* because it is outside the Product Owner's core expertise (background: QA Lead in cross-functional software teams; not a professional developer). Validation is multi-case-study; Case Study #2 is the Career Engineering Framework (a knowledge product). If the same principles hold across a software project *and* a knowledge product, the transferable value is shown to live in **intentional Human–AI collaboration design**, not website-building. Explicitly held as a working hypothesis.

### 3.4 The platform's three jobs, layered over time
Identified that the platform carries three purposes: (1) Case Study #1, (2) reusable-knowledge resource, (3) personal proof-of-capability. The Product Owner clarified these are **successive layers of the same product**, not competing priorities:
- MVP optimizes for **demonstrating professional capability** (portfolio).
- Later iterations expand into a knowledge resource and transparent methodology documentation.
- The architecture must support this evolution from day one.

### 3.5 Tension: differentiator deferred vs. MVP pitch — *resolved*
**Raised:** the strongest differentiator (the AI-workflow story) lives in later phases, while the MVP is a conventional portfolio — risking a generic first release.

**Resolution — "lead with evidence, not claims":** the AI-collaboration story is intentionally *not* the central MVP claim, because the evidence won't yet exist. The MVP is honest about the present and introduces two ongoing projects as explicit **work in progress** (Personal Platform; Career Engineering Framework), inviting visitors to follow their evolution. Credibility first; the differentiating narrative strengthens as real artifacts accumulate. Governing principle: **never claim what you can't demonstrate with real work.**

### 3.6 Success criteria
Defined on three levels:
1. **Product** — deployed, aesthetically aligned, clearly communicative; *proud to share* is the hard bar.
2. **Opportunity** — used in CV/LinkedIn/applications; traffic from those sources; analytics showing genuine exploration; more meaningful recruiter responses vs. baseline (directional, not scientific).
3. **Process** — proof of delivering a sophisticated product without being a professional developer, via a deliberately designed Human–AI workflow. First validation only; full workflow validation is longer-term.

### 3.7 Constraints
- **Time (binding):** target 16 July 2026, extendable to ~20 July 2026 to preserve quality/architecture. Tied to the job search; not absolute.
- **Budget:** free infrastructure as MVP default; open to paid domain/hosting as an implementation trade-off.
- **Authenticity:** publish only defensible work; WIP labeled openly.
- **Privacy:** minimal; comfortable sharing publicly.
- **Priority order:** quality > architecture > date. **Cut scope before quality or architecture.**

### 3.8 Tension: 5-day window vs. quality vs. evolution-ready architecture — *resolved*
**Raised:** with the MVP date ~5 days out (from 2026-07-11), "proud-to-share quality," "evolution-ready architecture," and "ship by the 16th" compete.

**Resolution:** explicit priority order — **quality first, architecture second, date third.** The date may slip to ~20 July. Scope is the release valve; features are cut before standards.

---

## 4. Facilitator self-review and gap closure

At the Product Owner's request, a critical self-review was performed. Findings and resolutions:

| Area | Finding | Resolution |
|---|---|---|
| Inconsistency | Free-infrastructure budget vs. professional-credibility bar (custom domain) | Reclassified as an **implementation trade-off**; recommendations to be provided during implementation. |
| Inconsistency | "Technically sophisticated" vs. "smallest MVP" | Confirmed: sophistication is demonstrated by the **engineering process**, not feature count. Product stays intentionally small. |
| Promote to decision | Language unstated | **English primary**; German and Ukrainian planned for future iterations. |
| Promote to decision | Surname-change requirement | Kept as a **product constraint** to honor; mechanics deferred to Architecture. |
| Promote to decision | WIP transparency | Confirmed as a first-class product concern. |
| Promote to decision | Analytics implied by success criteria | **Basic, privacy-conscious analytics are in the MVP**; solution is an implementation decision. |
| Risk | Content readiness | Retired — a substantial existing knowledge base will be used during implementation. |
| Risk | Timeline realism | Mitigated by the "cut scope first" rule and a defined MVP scope boundary. |
| Risk | Attribution of success signals | Accepted as a **known limitation**; signals are directional. |
| Risk | Sustainability of the "follow the evolution" promise | Noted; to be managed at a sustainable pace. |
| Gap | MVP scope boundary undefined | **Closed** — explicit in-scope and deferred lists agreed (see `PROJECT.md` §6–§7). |

---

## 5. Outcome summary

Shared understanding was reached across every required dimension: why the project exists, target audience, product vision, value proposition, MVP, long-term evolution, constraints, success criteria, and assumptions. See [`PROJECT.md`](../../PROJECT.md) for the canonical definition.

---

## 6. Lessons Learned

Lessons Learned

- Asking one question at a time kept the discussion focused.
- Self-review identified several genuine gaps that would otherwise have reached PROJECT.md.
- Separating Product Discovery from Architecture prevented premature technical decisions.
- Explicitly documenting tensions improved decision quality.
- Evidence-first positioning emerged naturally through the interview rather than being predefined.
## 6. Definition of Done

- [x] The Product Owner confirms the understanding.
- [x] No critical product questions remain.
- [x] Sufficient context exists to create `PROJECT.md`.

**Product Discovery is complete.** The next phase is **Engineering Architecture**.
