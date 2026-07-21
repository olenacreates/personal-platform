# Workshop 01 — Closure Summary

**Architecture Sprint · Workshop 01**
**Topic:** Architecturally Significant Requirements (ASR) Identification & Quality Attribute #1
**Participants:** Product Owner, ChatGPT (Product Owner collaborator), Claude (Lead Software Architect)
**Status:** ✅ Closed

---

## Workshop objective

Identify and evaluate candidate Architecturally Significant Requirements (ASRs), and establish the architectural direction for the first Quality Attribute.

---

## Main topics discussed

- Candidate ASRs derived from `PROJECT.md`, the Product Discovery Report, existing ADRs, and the engineering principles.
- The distinction between **Product Quality Attributes** (properties the system has) and **Engineering Practices** (how confidence in those properties is obtained).
- **Testability** evaluated as an architectural property vs. a Quality Engineering Strategy concern.
- The relationship between Maintainability, Understandability, Learnability, and Legibility as candidate framings for Attribute #1.
- ISO/IEC 25010 terminology vs. project-specific interpretation, and how far to extend a standard before it becomes a bespoke, hard-to-trace term.
- Downstream implications for a possible future Product Discovery amendment (audience scope).

---

## Working decisions reached

### Quality Attribute #1 — Maintainability, interpreted as *Architectural Legibility*

The project adopts **ISO/IEC 25010 Maintainability** as the official, standard-traceable Quality Attribute name. The project-specific interpretation of that attribute is named **Architectural Legibility**, and is described — not as a replacement term, but as the concrete lens through which Maintainability is understood and evaluated in this project.

**Architectural Legibility** means an architecture that is:

- understandable by inspection;
- maintainable by a non-specialist Product Owner working with AI assistance;
- reusable as a reference implementation for other practitioners;
- supported by explicit architectural rationale rather than implicit knowledge.

#### ISO/IEC 25010 mapping

- **Maintainability** (parent characteristic)
  - **Modularity** — clear separation of concerns, so a change in one area doesn't ripple unpredictably.
  - **Analysability** — how easily the system's behavior and structure can be understood by inspection.
  - **Reusability** — assets and patterns usable beyond their original context.
- **Extension:** Analysability is read here for a reader who is *studying* the system, not only one *maintaining* it — the practical consequence being that decisions require stated rationale (ADRs), not just clean code.

#### Architectural intent statement

> The architecture favors clarity, conventional patterns, and explicit rationale over cleverness or premature abstraction, so that the Product Owner — a non-specialist working with AI assistance — can confidently maintain and extend the system, and so that an external reader can understand the reasoning behind key decisions and adapt the approach to their own projects.

#### Quality scenario (ATAM style)

> **Stimulus:** An engineer unfamiliar with the project (e.g., a peer practitioner evaluating the Human–AI Engineering Workflow) clones the repository and reads the ADRs and top-level structure.
> **Environment:** No prior context beyond what's in the repository; no walkthrough from the Product Owner.
> **Response:** The engineer can correctly explain the site's information architecture and the reasoning behind the framework choice (ADR-005) without running the code or asking clarifying questions.
> **Response measure:** Achieved within a single reading session (target: under 30 minutes), verified informally by asking a real outside reader to attempt it.

#### Architectural decisions this attribute is expected to influence

- Framework/tooling choice (ADR-005) — simplicity and mainstream-recognizability weighed alongside other evaluation criteria.
- Repository and component structure — conventional, discoverable organization over clever or highly customized abstraction.
- ADR and documentation conventions — continued investment in stating rationale and alternatives-considered, not just decisions.
- Content/code comment density where non-obvious rationale exists.

This is the working baseline for the future Quality Attributes artifact.

---

## Important decisions

- **Maintainability** remains the official, ISO-traceable Quality Attribute name for this slot.
- **Architectural Legibility** is the project's named interpretation of that attribute, described inside the Quality Attributes artifact — not a competing or replacement term.
- The project-specific interpretation **extends**, rather than replaces, ISO/IEC 25010.
- **Testability will not become an independent ASR** — it is achieved as a byproduct of the Maintainability/Evolvability decisions (content/layout separation per ADR-002, identity-as-config per ADR-003).
- Testability **as engineering practice** belongs in the future Quality Engineering Strategy artifact (backlogged, not part of this sprint).
- **Security** remains baseline engineering hygiene — not a ranked ASR, no dedicated scenario required.
- **Reliability** is deferred as a future architectural consideration.
- **Traceability** belongs to process, not product architecture.
- **Transparency** (work-in-progress / "follow the evolution") belongs to Content Architecture, not Quality Attributes.
- Possible expansion of the intended audience (explicit teaching artifact for junior/mid-level engineers, beyond `PROJECT.md` §3's confirmed audience) has been identified as a **potential Product Discovery amendment**, not an architecture decision, and is not resolved by this workshop.

---

## Open items intentionally deferred

1. **Audience-scope question** — whether `PROJECT.md` §3 should be amended to include junior/mid-level engineers as a teaching audience, or whether the current practitioner-focused audience stands as-is.
2. **Reliability** — not yet evaluated; parked for a future workshop or the final Architecture Review.
3. **Build-time content validation** as a testability affordance — flagged as a specific question to raise during the Technology Evaluation Results review (ADR-005), not resolved here.
4. **Remaining candidate ASRs not yet fully evaluated**: Evolvability, Performance, Privacy-conscious analytics, SEO/discoverability — identified in the earlier candidate analysis but not yet carried through the same depth of discussion as Attribute #1.
5. Whether the eventual **Quality Attributes artifact** lives at `docs/architecture/quality-attributes.md` or elsewhere — a placement decision, not yet made.

---

## Deliverables produced by this workshop

Inputs now ready to feed the future Quality Attributes artifact:

- One fully specified Quality Attribute: standard name (Maintainability), project interpretation (Architectural Legibility), ISO/IEC 25010 mapping with stated extension, intent statement, one ATAM-style scenario, list of architectural decisions it influences.
- A clear, reusable **rule for classifying candidate ASRs**: product property → Quality Attributes artifact; verification practice → Quality Engineering Strategy artifact; process concern → elsewhere (backlog/process docs); baseline hygiene → not ranked at all. This rule is itself a reusable piece of the Human–AI Engineering Workflow, independent of this specific project.
- A backlog entry for the future **Quality Engineering Strategy** artifact (parked during this sprint).
- A flagged, unresolved **Product Discovery amendment candidate** (audience scope).

---

## Readiness assessment

**Workshop 01 is complete.** The workshop's objective — establishing a repeatable method for evaluating candidate ASRs, and producing one fully reasoned, scenario-backed Quality Attribute as a working baseline — has been met. Per the project's own engineering principles ("build the smallest implementation that preserves the long-term architecture"; "invest after validation"), continuing to refine Attribute #1 further now would trade sprint throughput for marginal wording polish, when the more valuable next step is applying the now-validated method to the remaining candidate ASRs. The open items above are appropriately deferred, not swept aside — none of them block moving forward.

---

## Recommended next step

**Workshop 02 — Evolvability**, evaluated with the same rigor established here (candidate analysis → ISO/IEC 25010 mapping if applicable → intent statement → scenario → influenced decisions). Evolvability is the attribute most directly load-bearing on the framework decision already pending (ADR-005), and is already tightly coupled to two accepted ADRs (i18n-readiness, identity-independence) — resolving it next keeps the dependency chain toward ADR-004/ADR-005 intact.
