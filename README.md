# Service POC Portfolio

This repository is the central record for a portfolio of distinct service-product proofs of concept. It holds shared working standards and each project's product, design, and planning documents. A project's application code may live in its own repository; link that repository from the project's README when it exists.

## Start here

- [Project catalog](portfolio/project-catalog.md) — ten candidate POCs; none selected yet
- [Current workflow](shared/workflow/workflow.md) — the shared process for future projects
- [Salon Booking](projects/salon-booking/README.md) — the existing project's current documents
- [Starting a project](projects/README.md) — how a new project session should use this repository

## Repository map

```text
portfolio/                 Candidate projects and selection decisions
shared/workflow/           Current cross-project workflow and future observations
projects/salon-booking/    Existing project documents
projects/<project-slug>/   Add only when a new project is selected
```

## Documentation rules

1. Put a rule or process used across projects in `shared/`. Put product requirements, design, prompts, and implementation decisions in that project's directory.
2. Every project has a `README.md` with its purpose, status, document index, and links to its code or prototype when available.
3. Create a project directory only after that project is selected in its own session. A catalog entry is an idea, not an active project.
4. Keep current decisions in canonical documents. Replace a superseded draft instead of leaving multiple competing source-of-truth files; Git retains earlier revisions.
5. Record new workflow observations separately and update the current workflow deliberately when evidence warrants it.

The GitHub repository is the durable documentation record. Once a POC is exported for engineering, its own code repository becomes the source of truth for implementation, as described in the [current workflow](shared/workflow/workflow.md).
