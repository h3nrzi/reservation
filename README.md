# Service POC Portfolio

This repository is the central record for a portfolio of distinct service-product proofs of concept. It holds shared working standards and each project's product, design, and planning documents. A project's application code may live in its own repository; link that repository from the project's README when it exists.

## Start here

- [Project catalog](portfolio/project-catalog.md) — the ten candidate POCs and their distinct product problems
- [Shared workflow](shared/workflow/README.md) — v0.2 for new POCs, v0.1 history, and the feedback log
- [Salon Booking](projects/salon-booking/README.md) — the existing project and its documents
- [Project documentation guide](projects/README.md) — where to put documents for future POCs

## Repository map

```text
portfolio/                 Portfolio choices and project catalog
shared/workflow/           Cross-project workflow and evidence for improvements
projects/<project-slug>/   Documents and prompts for one product
```

## Documentation rules

1. Put a rule or process used across projects in `shared/`. Put product requirements, design, prompts, and implementation decisions in that project's directory.
2. Every project has a `README.md` with its purpose, status, document index, and links to its code or prototype when available.
3. Add a project directory when work on that project begins. Catalog entries alone do not imply a project has started.
4. Keep important decisions in repository documents rather than only in chat history. Record workflow observations in the shared feedback log; change the workflow version deliberately.
5. Preserve the original versioned documents. New versions should make their status and relationship to earlier versions clear.

The GitHub repository is the durable documentation record. Once a POC is exported for engineering, its own code repository becomes the source of truth for implementation, as described in the [current workflow](shared/workflow/workflow-v0.2.md).
