# Human–AI Collaboration Model

**Status:** Draft  
**Owner:** Olena Lendiel  
**Last Updated:** 2026-07-23

---

# Why this document exists

The Human–AI Engineering Workflow is more than a sequence of engineering activities.
It also defines **how humans and AI collaborate** throughout software development.

To keep collaboration explicit and reusable, the workflow separates four independent dimensions:

- Role
- Interaction Mode
- Protocol
- Artifact

Each answers a different question and should evolve independently.

---

# Collaboration Model

| Dimension | Question | Purpose |
|-----------|----------|---------|
| **Role** | Who is responsible? | Defines the perspective, responsibilities, and expertise the AI adopts. |
| **Interaction Mode** | How do we communicate? | Defines the communication style and expected depth of interaction. |
| **Protocol** | How is the work performed? | Defines the sequence of activities for a specific workflow. |
| **Artifact** | What is produced? | Defines the expected output of the work. |

These dimensions intentionally remain independent.

The same Role may operate using different Interaction Modes.

The same Protocol may produce different Artifacts.

This separation makes the workflow easier to evolve without tightly coupling responsibilities, communication style, process, and outputs.

---

# Roles

Roles define **who the AI is** during a particular activity.

Examples include:

- Product Discovery Facilitator
- Engineering Architect
- Implementation Engineer
- QA Reviewer
- Learning Coach

A role determines:

- responsibilities
- mindset
- decision criteria
- expertise applied

A role does **not** determine communication style.

---

# Interaction Modes

Interaction Modes define **how the conversation happens**.

The same Engineering Architect may participate in a short discussion, facilitate a workshop, write documentation, or review an artifact.

## Discussion Mode

Purpose

Explore ideas efficiently.

Characteristics

- concise
- conversational
- one topic at a time
- one recommendation
- one next step

Primary output

Shared understanding.

---

## Workshop Mode

Purpose

Explore a problem deeply before making decisions.

Characteristics

- structured reasoning
- alternatives
- trade-offs
- collaborative thinking

Primary output

Workshop notes and architectural decisions.

---

## Documentation Mode

Purpose

Produce repository artifacts.

Characteristics

- minimal discussion
- focus on correctness and consistency
- follows repository conventions

Primary output

Documents such as ADRs, architecture descriptions, reports, and READMEs.

---

## Review Mode

Purpose

Critically evaluate existing work.

Characteristics

- verify evidence
- challenge assumptions
- identify gaps
- avoid rubber-stamping conclusions

Primary output

Review comments, requested changes, or approval.

---

# Protocols

Protocols define **how work is organized**.

Examples:

- Product Discovery
- Architecture Decision Review
- Sprint Closure
- ADR Review

A protocol describes the sequence of activities.

It does not prescribe the communication style.

---

# Artifacts

Artifacts are the tangible outputs produced by the workflow.

Examples include:

- ADRs
- Architecture documents
- Product Discovery Report
- Engineering Principles
- Insights
- Decision Frameworks

Artifacts capture reusable knowledge rather than conversations.

---

# Design Principles

This model intentionally separates:

- responsibility,
- communication,
- workflow,
- output.

Changing one dimension should not require changing the others.

For example:

The Engineering Architect role may operate in Discussion Mode while exploring ideas, switch to Documentation Mode when writing ADR-005, and later enter Review Mode to evaluate implementation.

The role remains the same.

Only the interaction mode changes.

---

# Future Evolution

The model is expected to evolve as additional projects validate new collaboration patterns.

Interaction Modes, Roles, Protocols, and Artifact types should emerge from practice rather than be designed upfront.