# PROJECT.md

> Canonical product definition for the Personal Platform.
> Produced by **Protocol 01 — Project Discovery**. Confirmed by the Product Owner on 2026-07-11.
> This document defines the *product*. It does not define architecture or implementation — those belong to the Engineering Architecture and Implementation phases.

---

## 1. What this project is

This repository is an experiment in **Designing an AI Engineering Workflow**.

Its purpose is not only to build a production-quality personal platform, but to design, validate, and document an effective way for humans and AI to collaborate throughout the software development lifecycle.

- **Primary outcome:** a validated, documented AI Engineering Workflow. *(ADR-001)*
- **Secondary artifact:** a personal professional platform, produced by running that workflow — serving as **Case Study #1**.

The platform is the first validation of the workflow, not its final proof. Full validation is expected to require multiple case studies across different kinds of work (Case Study #2: the Career Engineering Framework, a knowledge-intensive product).

---

## 2. Why this project exists

A single system with four parts:

- **Goal** — design and validate an AI Engineering Workflow.
- **Approach** — systems thinking and learning through building.
- **Primary deliverable** — reusable knowledge (workflow, protocols, practices).
- **Intended impact** — sharing that knowledge with the community.

The bar is **knowledge reusable by others**, not personal learning. This distinction shapes how the project is documented and how success is judged.

Core hypothesis under test:

> Can someone with strong engineering understanding — but without professional software-development experience — successfully deliver a complex technical project by designing an effective Human–AI collaboration workflow?

Guiding belief (an application of the Product Owner's Career Engineering Framework): meaningful career development happens by designing real systems, running experiments, and creating reusable knowledge through practice rather than only consuming information.

The aspiration: demonstrate that **AI can be a thoughtful engineering collaborator, not just a code generator.**

---

## 3. Target audience

**Ultimate audience (the methodology):** professionals with strong domain expertise who are still figuring out how to collaborate effectively with AI in daily work — people transitioning into technical roles and technical-adjacent professionals outside software engineering (QA engineers, TPMs, business analysts, product managers, Scrum Masters, engineering managers). Unified by a shared *need* — to design an intentional way of working with AI rather than using disconnected prompts — not by job title.

The goal is **not** to teach a specific AI tool. It is to help people build **their own** Human–AI collaboration workflow that fits their context, work, and thinking.

**MVP audience (the platform, Release 1):** hiring managers, recruiters, potential collaborators, and conference organizers.

---

## 4. Product vision

A personal platform that evolves in **successive layers over time** — from a professional portfolio into a reusable knowledge resource and a transparent, documented record of the workflow methodology.

The three purposes are layered, not competing:

1. **MVP:** demonstrate professional capability (portfolio).
2. **Later:** become a reusable knowledge resource for the community.
3. **Later:** transparently document the methodology and its evolution.

The architecture must support this long-term evolution from day one, even though Release 1 implements only a small slice of it.

---

## 5. Value proposition

**Lead with evidence, not claims.**

The Human–AI collaboration story is expected to become the platform's strongest differentiator, but it is deliberately **not** the central claim in the MVP, because sufficient evidence will not yet exist.

Governing principle: **never make claims that cannot be demonstrated with real work.** The MVP is honest about where the Product Owner is today; the differentiating narrative strengthens naturally as real artifacts (protocols, case studies, documentation, validated practices) accumulate.

Technical sophistication is demonstrated through the **engineering process** — intentional Human–AI collaboration, well-designed workflows and protocols, engineering documentation, architecture, decision-making, and quality practices — **not** through the number of product features. The product stays intentionally small while demonstrating mature engineering thinking.

---

## 6. MVP scope (Release 1)

**Sections:**

- **Home** — answers: Who am I? · What problems do I solve? · What kind of work do I do? · Why should someone work with me?
- **About**
- **Professional Experience**
- **Selected Projects** — introduces two ongoing projects as explicit **work in progress**, inviting visitors to follow their evolution over time:
  - Personal Platform
  - Career Engineering Framework
- **Community & Knowledge Sharing** — the long-term, evergreen, structured home for activity that otherwise disappears in the LinkedIn feed. Presents both initiatives the Product Owner participates in and initiatives she creates. Examples: Employee Engagement Program, Women ERG, internal learning initiatives, workshops, conference talks, mentoring, and future community collaborations (e.g. WIT UA, Ukrainian IT Cluster). Upcoming activities appear under an **"Upcoming"** section and graduate into permanent portfolio entries — documenting the initiative and its outcomes — once completed.
- **Contact**

**Also in MVP:**

- **Basic, privacy-conscious analytics** — required to evaluate the product success criteria. (The specific solution is an implementation decision.)

---

## 7. Explicitly deferred from MVP

Out of scope for Release 1. The architecture should *support* these future capabilities, but they are not required:

- AI Protocol Library
- Learning Notes
- Engineering Articles
- Case Studies
- Workshop Materials
- Blog
- Newsletter
- Search
- CMS

---

## 8. Long-term evolution

Successive layers of the same product, expanding into the deferred sections above, plus multi-language support (see §10).

---

## 9. Constraints

- **Priority order when constraints conflict:**
  1. Quality — *proud to share*.
  2. A sound architectural foundation that allows the platform to evolve.
  3. The target date.

  When time is the limiting factor, **reduce scope before sacrificing quality or architecture.** Avoid perfectionism by cutting features, not standards.
- **Timeline:** target deployment **16 July 2026**, extendable to **~20 July 2026** if the extra time preserves both quality and architectural integrity. The date supports the job search and interviews but is **not** an absolute constraint.
- **Budget:** free infrastructure is the default for the MVP. Open to a paid custom domain and hosting if it meaningfully improves professional presentation — treated as an **implementation trade-off**, pending practical recommendations.
- **Authenticity:** publish only work that can be genuinely stood behind. Unfinished sections are presented openly as "work in progress," never faked as complete.
- **Privacy:** minimal constraints; comfortable sharing work, learning process, and methodology publicly.

---

## 10. Key decisions (explicit)

- The **workflow is the primary outcome**; the website is Case Study #1. *(ADR-001)*
- **Languages:** English is the primary language. German and Ukrainian are planned as supported languages in future iterations.
- **Work-in-progress transparency** ("follow the evolution") is a first-class product concern.
- Basic, privacy-conscious **analytics** are part of the MVP (solution TBD in implementation).

---

## 11. Success criteria

1. **Product success** — a deployed website whose design reflects the Product Owner's aesthetic and clearly communicates her professional experience, strengths, and the work she wants to do. Hard bar: **if she is not proud to share it, it is not successful.**
2. **Opportunity success** — the platform creates professional opportunities. Included in CV, LinkedIn, and job applications. Directional signals sought: visitors arriving from LinkedIn and applications; analytics showing people actually explore the site; an increase in meaningful responses from recruiters and hiring managers versus the current job search.
3. **Process success** — proof that the Product Owner can deliver a technically sophisticated product despite not being a professional developer, and — more importantly — that a carefully designed Human–AI collaboration workflow enables someone with strong engineering thinking to complete work previously outside their practical skill set.

The website is the **first** validation of the process hypothesis. Full workflow validation is a longer-term question requiring multiple case studies.

---

## 12. Assumptions and known limitations

- The transferable value of the workflow (beyond software) is a **working hypothesis** to be validated across multiple case studies, not assumed.
- Opportunity-success signals (recruiter/hiring-manager responses) are **directional evidence, not scientific measurement**; attribution is confounded by market conditions, CV changes, and timing.
- Content for the platform will be generated and refined during implementation from an existing, substantial knowledge base — **not** a discovery concern.

---

## 13. Deferred to Engineering Architecture / Implementation

The following are recognized as **design decisions**, not product decisions, and are intentionally left to later phases:

- Surname independence — the platform's identity, URLs, and branding must absorb a likely future surname change (following the Product Owner's divorce) without major restructuring or broken links. *(Product constraint to honor during design.)*
- Implementation mechanics of work-in-progress content and the "follow the evolution" experience.
- Custom-domain and hosting decision.
- Analytics solution selection.
- Content generation and refinement.

---

## Definition of Done — Product Discovery

- [x] Product Owner confirms the understanding (2026-07-11).
- [x] No critical product questions remain.
- [x] Sufficient context exists to create this `PROJECT.md`.

**Next phase:** Engineering Architecture.
