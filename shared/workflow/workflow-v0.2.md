# Controlled Vibe Coding Workflow

**Version:** 0.2

**Status:** Active for new POCs / under evaluation

**Supersedes:** v0.1 for projects started after Salon Booking

## Purpose

This workflow defines a controlled approach for building production applications using AI-assisted development.

The goal is to combine:

- Base44 for rapid frontend and UX prototyping
- Dummy/mock data during frontend exploration
- Local Git as the source of truth after prototyping
- Codex for engineering, architecture, and implementation
- Matt Pocock-inspired planning and implementation practices
- Explicit specifications, tickets, reviews, and quality gates

The workflow is intentionally evolutionary.

Real project experience takes precedence over preserving previous workflow decisions. Problems discovered while using the workflow should be recorded and considered for future versions.

This version incorporates [WF-001 through WF-007](workflow-feedback.md) from Salon Booking. Their adoption is a process decision, not proof that every change has been validated across projects. Record the result of using them on the next POC.

The central portfolio repository stores shared workflow and project documents. After a prototype is exported, the product's code repository is the authority for implementation and technical decisions. Link the two records from the project README.

---

# Core Principle

Base44 is primarily a product and UI prototyping environment.

It should help us discover and build the user experience quickly, but it should not automatically become the authority for the final application architecture.

After the prototype is exported/ejected:

> The local Git repository becomes the source of truth.

Generated code should be evaluated rather than blindly preserved.

---

# Phase 0 — Product Discovery

Before using Base44, define the product at a high level.

Capture:

- Problem
- Target users
- Core use cases
- User roles
- Major business rules
- Non-goals
- Open questions

Initial artifact: `product-brief.md` in the project's documentation directory.

Before deciding routes or asking Base44 to create pages, work through this sequence:

1. **Locale and market requirements:** Decide or explicitly defer language, writing direction, script and typography, numerals, calendar, date/time formatting, currency, locale-specific sample content, directional UI behavior, and internationalization scope. Capture the result in `locale-requirements.md`. Do not require a full i18n architecture unless the product needs one. *(WF-005)*
2. **Core journeys:** Describe what each user role needs to accomplish, including important alternate and failure paths. Capture them in `core-journeys.md`. *(WF-001)*
3. **Capability map:** Group the capabilities needed to support those journeys without treating every capability as a page. Capture them in `capability-map.md`. *(WF-001)*
4. **POC/MVP boundary:** Mark capabilities as in scope, later, or unresolved. Do this before final page planning so future features do not silently enter the prototype. Record the boundary in the capability map or a separate scope document. *(WF-002)*
5. **Candidate page inventory:** List candidate screens after the scope boundary. Classify routes, nested views, booking or task steps, tabs, drawers, and dialogs rather than equating each step with a page. *(WF-001)*
6. **Route and screen decisions:** Resolve the navigation and layout implications, then approve a `page-manifest.md` for the prototype. *(WF-001)*
7. **Design direction:** Agree on visual character, audience, density, imagery, and accessibility goals before choosing token values. Capture this in `design-direction.md`. *(WF-003)*

The sequence is a decision order, not a demand for seven elaborate documents. Keep each artifact only as detailed as the next decision needs. Do not make detailed backend or database decisions at this stage.

---

# Phase 1 — UI Foundation

Before implementing individual pages, establish the frontend foundation.

## 1. Approved Page Manifest

Use the approved page manifest from Phase 0 before asking Base44 to design screens.

Base44 should understand the approximate overall shape and size of the application from the beginning.

## 2. Placeholder Pages

Create all known routes/screens as placeholders first.

Each placeholder should contain only enough information to identify the screen.

Do not allow Base44 to invent full page designs during this pass.

## 3. Layout Taxonomy

Identify the major application layouts before page implementation.

Examples:

- Public layout
- Authentication layout
- Customer application layout
- Admin/management layout
- Settings layout

Avoid duplicating application shells across pages.

## 4. Design Tokens

Translate the approved design direction and locale requirements into a visual system before individual page design. *(WF-003, WF-005)*

Tokens should cover relevant decisions such as:

- Colors
- Typography
- Radius
- Shadows
- Layout dimensions
- Semantic states

Use the dependency direction **primitive tokens → semantic tokens → component variants/usage → UI**. Primitive values belong in the token foundation; application components should use semantic tokens where an appropriate token exists. Do not demand exhaustive tokens before there is evidence for them. *(WF-004)*

Examples of semantic tokens:

- background
- foreground
- surface
- primary
- primary-foreground
- muted
- muted-foreground
- border
- success
- warning
- danger

Avoid scattering raw visual values throughout components when a design token exists. Review generated output for accidental coupling to primitive colors or one-off values.

Do not override standard Tailwind scales without a design reason.

## 5. Tailwind Foundation

Configure the project's styling system around the approved design tokens.

The design system should become the source of truth for future page implementation.

## 6. Foundation Stop

After:

- routing
- layouts
- placeholder pages
- design tokens
- styling foundation
- correct locale and direction behavior

Base44 must stop.

The foundation should be reviewed before actual page design begins.

---

# Phase 2 — Shared UI Foundations

Create reusable UI primitives required by the product.

Examples may include:

- Button
- Input
- Select
- Checkbox
- Dialog
- Dropdown
- Tabs
- Table primitives
- Form primitives

Do not prematurely create large application-specific abstractions.

Stop and review the shared foundation before proceeding.

---

# Phase 3 — Incremental Page Implementation

Implement pages incrementally rather than asking Base44 to generate the entire application in one pass.

Preferred loop: **Page spec → Page prompt → Generate → Product/structure review → UI review → Log UI debt → Accept prototype page → Next page.** *(WF-006)*

Correct a blocking issue before moving on when a page is unusable, structurally wrong, or misleading. Record non-blocking visual issues in a centralized UI refinement backlog for the later local/Codex pass. A backlog item should identify the page, issue, severity, likely scope (global, component, or page), and proposed remedy. Do not use repeated Base44 generation cycles for routine polish when the local pass can resolve it more efficiently.

Base44 should use deterministic dummy/mock data.

During this phase:

- No production backend
- No production database
- No unnecessary infrastructure
- No premature backend architecture

The primary objective is validating product UX.

---

# Phase 4 — Cross-Page UX

After the major pages exist, review the application as a complete experience.

Review:

- Navigation
- Responsive behavior
- Loading states
- Empty states
- Error states
- Form states
- Accessibility
- Visual consistency
- Interaction consistency
- Cross-page user journeys
- Recorded UI debt and which issues block prototype approval

---

# Phase 5 — Prototype Freeze

Once the frontend experience is approved at the prototype level, create a prototype checkpoint. Non-blocking visual debt may remain in the backlog; blocking product or usability issues may not.

The prototype represents:

> What the product should do and how the user should experience it.

It does not represent the final engineering architecture.

After this checkpoint, export/eject the project from Base44.

Record the prototype link or export reference and the remaining UI refinement backlog in the project README.

---

# Phase 6 — Local Repository Becomes Source of Truth

After export/eject:

> Local Git repository = Source of Truth

Base44-generated architecture is treated as input, not as an unquestionable architectural foundation.

Base44 may still be used for isolated product/UI exploration, but production engineering decisions happen in the local repository.

After architecture assessment and before backend integration, address the UI refinement backlog in this order: system/token issues, shared component issues, page-specific issues, then responsive and accessibility QA. Recheck the cross-page journeys after these fixes. *(WF-006)*

---

# Phase 7 — Engineering Discovery

Codex must not immediately start refactoring or building the backend.

First perform repository and product discovery.

Use a Matt Pocock-inspired approach:

Grill
→ Clarify
→ Plan

Investigate:

- Product assumptions
- Domain concepts
- Existing frontend architecture
- State management
- Data boundaries
- Authentication
- Authorization
- Validation
- Error handling
- API boundaries
- Testing
- Security
- Deployment
- Observability
- Relevant edge cases

Unresolved questions should be surfaced before major implementation begins.

---

# Phase 8 — Architecture Assessment

Evaluate the Base44-generated application.

Document:

`current-state.md`

Including:

- Existing architecture
- State locations
- Data access
- Component structure
- Coupling
- Duplication
- Technical debt
- Useful generated patterns
- Disposable prototype scaffolding

Then define:

`target-state.md`

The target architecture should be based on actual project requirements rather than mechanically preserving generated architecture.

Important architectural decisions should be captured as ADRs when appropriate.

---

# Phase 9 — Domain Modeling

Before designing the backend around database tables, establish shared domain language.

Create:

`domain/glossary.md`

Identify:

- Entities
- Concepts
- Relationships
- Important business terminology
- Business rules

Preferred direction:

Domain
→ Use Cases
→ API Contract
→ Persistence

Rather than:

Database
→ Everything Else

---

# Phase 10 — Contract First

Define the frontend/backend boundary before tightly coupling the frontend to a real backend.

The frontend should interact through explicit application/data interfaces.

During prototyping:

UI
→ Interface
→ Mock Implementation

Later:

UI
→ Same Interface
→ API Implementation
→ Backend

The goal is to replace the mock implementation without rewriting the UI.

---

# Phase 11 — Specification

Convert clarified requirements and architectural decisions into implementation specifications.

Preferred workflow:

Grill
→ Spec
→ Tickets

Specifications should define:

- Scope
- Requirements
- Constraints
- Important decisions
- Acceptance criteria
- Relevant edge cases
- Non-goals

---

# Phase 12 — Tickets

Break specifications into small implementation units.

Prefer vertical slices over large horizontal infrastructure projects.

Prefer:

User can view a service request end-to-end.

Over:

Build the entire backend layer.

Tickets should be small enough to implement and verify within a focused context.

---

# Phase 13 — Implementation Loop

For each ticket:

Fresh Context
→ Read Ticket
→ Read Relevant Documentation/ADRs
→ Inspect Relevant Code
→ Plan
→ Implement
→ Typecheck
→ Lint
→ Test
→ Review
→ Commit

Avoid using one long AI context for unrelated areas of the system.

Clear context between substantial tickets when appropriate.

---

# Phase 14 — Independent Review

Prefer reviewing implementation from a fresh context rather than relying exclusively on the context that wrote the code.

Review on two axes:

## Specification Review

Does the implementation satisfy the intended behavior and acceptance criteria?

## Engineering Review

Does the implementation satisfy repository architecture, maintainability, testing, security, and engineering standards?

---

# Phase 15 — Mock to Real Backend

Once backend capabilities exist, replace mock adapters incrementally.

Before:

UI
→ Application Interface
→ Mock Implementation

After:

UI
→ Application Interface
→ API Implementation
→ Backend
→ Database

The UI should not require substantial restructuring simply because the data source changed.

---

# Phase 16 — Vertical Integration

Integrate backend capabilities feature by feature.

Example:

Service Request List
→ API Client
→ Endpoint
→ Application Service
→ Repository
→ Database
→ Tests

Complete and verify one vertical slice before expanding unnecessarily.

---

# Phase 17 — Production Hardening

After core product flows work, perform explicit production-readiness work.

Review relevant areas including:

- Authentication
- Authorization
- Input validation
- Rate limiting
- Secrets
- Logging
- Observability
- Database migrations
- Database indexes
- Backup and recovery
- Error handling
- Timeouts
- Retries
- Idempotency
- Performance
- Accessibility
- Responsive QA
- Security review
- Deployment

---

# Cross-Cutting Rule — Expiring Tool Budgets

When a tool has credits or capacity that will expire or reset, check the remaining budget after the primary planned work. If useful, already-understood backlog work fits, complete a bounded low-risk item before reset. Prefer a small known fix, UI cleanup, or relevant QA over speculative analysis. Leaving unused capacity is acceptable. *(WF-007)*

Do not create work merely to consume quota. Do not use a reset window to justify new features, risky architecture changes, broad refactors, or work unlikely to finish within the remaining budget. If quota rolls over, use has a cost, or remaining capacity has future value, preserve it unless the planned work independently warrants spending it.

This rule changes scheduling, not the product scope or review gates.

---

# Repository Foundation

A typical repository may evolve toward:

```text
/
├── AGENTS.md
├── docs/
│   ├── product/
│   ├── domain/
│   ├── architecture/
│   └── adr/
├── specs/
├── tickets/
├── frontend/
├── backend/
└── tests/
```

The exact structure should follow project needs rather than being imposed unnecessarily.

---

# AGENTS.md

The local repository should eventually define instructions for coding agents.

Relevant areas may include:

- Planning rules
- Architecture rules
- Testing rules
- Definition of Done
- Git rules
- Security requirements
- Documentation requirements
- Forbidden actions
- Review expectations

---

# Workflow Evolution

This workflow is not considered final.

When project experience reveals a problem:

1. Do not silently rewrite the workflow.
2. Record the finding in `workflow-feedback.md`.
3. Continue with the best project decision when necessary.
4. Evaluate the finding for the next workflow version.

Record the workflow version used by each project in its project README. A newer shared version does not retroactively change the process record for an existing project.

For the first POC using v0.2, record evidence in the feedback log at these checkpoints:

- Did locale requirements prevent avoidable layout or content rework? *(WF-005)*
- Did journeys, capability map, scope boundary, and route classification produce a clearer page manifest without excessive process? *(WF-001, WF-002)*
- Did design direction and layered tokens make generated UI more consistent and easier to adjust? *(WF-003, WF-004)*
- Did the UI backlog let the team move through pages while still resolving important issues after export? *(WF-006)*
- Did the expiring-budget rule produce useful finished work without scope creep or waste? *(WF-007)*

Use the observations to revise the next version; do not mark these changes fully validated based only on Salon Booking.

Versioning guideline:

- Minor workflow refinements: `v0.3`, `v0.4`, etc.
- Stable initial workflow after sufficient real-world validation: `v1.0`
- Fundamental redesign after stabilization: future major version

Real project evidence has priority over preserving decisions from previous workflow versions.
