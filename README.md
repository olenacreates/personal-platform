# personal-platform

An engineering experiment, documented in public. I'm building a personal website
with AI and writing down how the work actually gets done.

## Status

- **Experiment:** designing a human–AI engineering workflow
- **Sprint:** 1 — Architecture Design
- **Research question:** Can AI design an architecture I'd be willing to maintain?

<!-- Update the research question each sprint as the experiment moves on. -->

## What this is

This repository is an experiment, not a product launch. The website is only the
case study. What's being built and tested is the **workflow** — how a human and AI
split the work, make decisions, and record them across the software lifecycle.

So, plainly: this is not another AI-generated website. The site is how I study the
collaboration. The workflow, and what it teaches about working with AI, is the real
output.

The workflow is the product. The website is **Case Study #1** ([ADR-001](docs/adr/adr-001.md)).
Later case studies will test whether the same workflow holds outside web development.
Expect the repository — and this README — to change as the experiment does.

## Why it's worth following

Most writing about AI in software stops at prompts and demos. This tries to record
the parts that usually stay invisible: where AI helped, where it got in the way,
which decisions were hard, and what I changed afterward. If you're working out how
to collaborate with AI on real engineering, these notes may be useful.

## Principles

- Curiosity before certainty.
- Build systems, not shortcuts.
- Treat AI as a collaborator, not an oracle.
- Document decisions, not conversations.
- Reduce scope before reducing quality.
- Learn in public.

## Engineering collaborators

- **ChatGPT** — day-to-day engineering collaboration
- **Claude** — architecture, writing, and implementation
- **Gemini** — milestone reviews and second opinions across the whole project

The human stays the Product Owner: sets direction, makes the decisions, approves
the work.

## How to navigate

| To see… | Look at |
|---|---|
| Product definition & MVP scope | [`PROJECT.md`](PROJECT.md) |
| Decisions, with rationale | [`docs/adr/`](docs/adr/) |
| How discovery actually went | [`docs/discovery/`](docs/discovery/) |
| What each sprint taught | [`docs/insights/`](docs/insights/) |
| The way we work | [`CLAUDE.md`](CLAUDE.md) · [`docs/core-principles/`](docs/core-principles/) |
| The SDLC protocols | [`protocols/`](protocols/) |
| The public series drafts | [`content/`](content/) |

## Feedback

This is a learning experiment, and review is welcome — most useful on the
requirements ([`PROJECT.md`](PROJECT.md)), the decision records
([`docs/adr/`](docs/adr/)), and any question I've missed. Open an Issue or a
Discussion.

## License

See [LICENSE](LICENSE).
