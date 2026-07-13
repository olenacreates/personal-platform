# Spike Insights — AI Engineering Environment

Spike goal: stand up and validate the AI engineering *environment and methodology* — not product features. This spike was both an engineering spike (build the supporting artifacts) and a learning experiment (test whether an intentionally designed Human–AI workflow adds measurable value). Each insight tags its reusable takeaway so the distinction between *validated hypothesis*, *engineering principle*, *workflow adoption*, and *future work* stays explicit.

## Insight 001 — A specialized phase-gate skill adds value through structure and discipline, not by finding more

### Observation

**Built:** a "Phase Readiness Reviewer" skill (a gate for the Product Discovery → Architecture Design transition). **Learned:** run head-to-head against an unaided baseline on the *real* discovery artifacts, both reached the same verdict, but the with-skill review was materially more structured, evidence-cited, and traceable, and it honored a hard "no implementation unless the gate opens" constraint.

### Why it matters

It tells us *where* a specialized skill earns its keep: not by surfacing more issues than a capable model already finds, but by making the output auditable, repeatable, and disciplined. It also separates two axes we had been conflating — the quality of the review *artifact* versus the calibration of its *verdict*.

### Evidence

`phase-readiness-reviewer-workspace/iteration-1/` — `with_skill/` produced the fixed 8-section report, Critical/Major/Minor classification, a Missing-ADRs list, `[general best practice]` labels, and an explicit no-code stance; `without_skill/` produced a looser, ad-hoc write-up and waved the project through as a "clean go." Comparable cost (~53.5k vs ~47.6k tokens).

### Reusable takeaway

- **[Validated hypothesis]** a purpose-built skill measurably improves review quality over a baseline Claude review.
- **[Adopt into workflow]** require a skill-vs-baseline comparison before investing in any new specialized skill — evidence, not intuition, justifies the tooling.
- **[Future work]** the verdict-calibration gap (see Insight 002).

## Insight 002 — A gate's real value is the ability to say "not yet"

### Observation

**Learned:** the unaided baseline confidently advanced a polished-but-imperfect project ("clean go, not proceed-with-reservations"); the intended reference verdict was "Ready with Conditions." The scarce, valuable behavior is *withholding* approval, not producing it.

### Why it matters

Both models and people over-trust well-written artifacts. If the methodology relies on a reviewer's judgment alone, thorough-looking work sails through. The gate has to be explicitly calibrated to convert unrecorded/under-supported decisions into gating conditions.

### Evidence

Baseline verdict "Go" with confidence; the skill also returned "Go" on the same input despite the intended "Ready with Conditions" — the calibration gap is documented in the skill's `FUTURE-WORK.md`.

### Reusable takeaway

- **[Engineering principle]** separate a review artifact's *quality* from its verdict's *calibration*; a gate that cannot say "not yet" is not a gate.
- **[Future work]** tighten severity thresholds (prose-only load-bearing decisions → Major) and add within-document consistency checks.

## Insight 003 — ADRs are most valuable when they record the roads not taken

### Observation

**Built:** a reusable `docs/adr/adr-template.md` and two conforming ADRs (i18n; identity/URL), created by reviewing real decisions rather than in the abstract. **Learned:** the terse ADR-001 (decision only, no context or consequences) is noticeably less reusable than an ADR that records alternatives and impacted artifacts.

### Why it matters

Reference-quality ADRs teach *reasoning*, not just outcomes; recording rejected options stops future readers from blindly reopening settled questions, and "Impacted Artifacts" gives traceability across `PROJECT.md`, `CLAUDE.md`, and other ADRs.

### Evidence

`docs/adr/adr-template.md`; ADR-002 and ADR-003 conform (Context / Decision / Alternatives considered / Consequences / Impacted Artifacts); ADR-001 remains the counter-example the readiness review flagged.

### Reusable takeaway

- **[Adopt into workflow]** the ADR template and its conventions (one decision per ADR; record alternatives; capture decisions, not conversations).
- **[Engineering principle]** distinguish project standards from general best practice and label the latter, so an outside recommendation is never mistaken for a decision the owner made.
- **[Future work]** align ADR-001 to the template (deferred documentation work).

## Insight 004 — Long-lived knowledge belongs in versioned artifacts, not chat

### Observation

**Built:** `CLAUDE.md` as the repository operating guide, and moved conventions, decisions, and backlog items into `PROJECT.md`, ADRs, the ADR template, and the skill's `FUTURE-WORK.md` — rather than leaving them in the working conversation.

### Why it matters

This repository documents *both* the product and the engineering methodology behind it. Chat history is ephemeral, unshareable, and invisible to future collaborators (human or AI); an operating guide and decision records are not.

### Evidence

`CLAUDE.md` (sources of truth, non-negotiables, working agreement); the conventions comment embedded in `adr-template.md`; deferred items captured in `FUTURE-WORK.md` instead of chat.

### Reusable takeaway

- **[Engineering principle / Adopt into workflow]** every durable decision, convention, or backlog item must land in a version-controlled artifact; if it only exists in chat, it does not exist.

## Insight 005 — The environment now supports first-class Git/PR collaboration, validated on one real case

### Observation

**Built:** a working AI engineering environment in which the AI collaborator operates Git and an authenticated GitHub CLI directly (branch, commit, PR) alongside the human. **Learned:** validating the readiness skill on a *single real case* was sufficient to demonstrate the concept — a full synthetic suite was not needed to decide it had value.

### Why it matters

The environment capability unblocks the whole workflow (artifacts, reviews, and handoffs live in Git). And validating on one real case first mirrors the project's existing "invest after validation" principle — it kept the spike small while still producing evidence.

### Evidence

GitHub CLI installed and authenticated by the Product Owner (the AI does not hold credentials); PR #5 opened from within the environment; the skill concept was accepted as validated after one real-artifact comparison, with three synthetic scenarios deferred to a regression suite.

### Reusable takeaway

- **[Validated hypothesis]** the environment supports a real Git/PR-based Human–AI workflow; credential-holding stays with the human.
- **[Engineering principle]** validate a methodology change on one real case before building the full evaluation apparatus.
- **[Future work]** the deferred regression suite, skill packaging, and trigger-description optimization.

## Retrospective

### What worked

- Validating the readiness skill on a single real case (the actual discovery artifacts) produced a clear value signal fast, without building a full evaluation suite.
- Reviewing ADRs one at a time surfaced the conventions in context and produced a reusable template.
- Keeping decisions and conventions in artifacts (`PROJECT.md`, ADRs, `CLAUDE.md`, the ADR template) kept the working context clean and shareable.
- The human-holds-credentials boundary let the AI operate Git, the GitHub CLI, and PRs without ever handling secrets.

### What didn't

- The skill reached the same verdict as the baseline ("Go") rather than the intended "Ready with Conditions" — the gate's verdict calibration isn't there yet.
- The skill's consistency check missed a within-document defect (duplicate headings) that the unaided baseline caught.

### What surprised us

- The specialized skill's value was structure, evidence, and traceability — not finding *more* issues; the unaided baseline surfaced substantively similar findings.
- A well-written project is precisely what a reviewer is most likely to wave through; the discipline to withhold "Go" turned out to be the scarce behavior.

### Changes to the workflow

- Promoted two generally-applicable principles to `docs/core-principles/engineering-principles.md`: *validate a methodology change on one real case before building the full apparatus*, and *durable decisions, conventions, and backlog items belong in version-controlled artifacts, not chat*.
- Adopt the ADR template and its conventions for all future ADRs.
- Require a skill-vs-baseline comparison before investing in a new specialized skill.
- Held back (kept in this document until more evidence): "separate artifact-quality from verdict-calibration" and "label general best practice vs. project standards."
- Deferred documentation/technical work (tracked, not lost): the skill's verdict-calibration fix and regression suite (`FUTURE-WORK.md`), and aligning ADR-001 to the template.
