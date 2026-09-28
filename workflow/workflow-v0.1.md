# Controlled Vibe Coding Workflow

**Version:** 0.1  
**Status:** Draft / In Use

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

---

# Core Principle

Base44 is primarily a product and UI prototyping environment.

It should help us discover and build the user experience quickly, but it should not automatically become the authority for the final application architecture.

After the prototype is exported/ejected:

> The local Git repository becomes the source of truth.

Generated code should be evaluated rather than blindly preserved.

---

# Phase 0 — Product Definition

Before using Base44, define the product at a high level.

Capture:

- Problem
- Target users
- Core use cases
- Main user journeys
- User roles
- Major business rules
- Known pages/screens
- Non-goals
- Open questions

Initial artifact:

`product-brief.md`

Do not make detailed backend or database decisions at this stage.

---

# Phase 1 — UI Foundation

Before implementing individual pages, establish the frontend foundation.

## 1. Page Inventory

Identify the expected application pages/screens before asking Base44 to design them.

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

Define the visual system before individual page design.

Tokens should cover relevant decisions such as:

- Colors
- Typography
- Radius
- Shadows
- Layout dimensions
- Semantic states

Prefer semantic tokens such as:

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

Avoid scattering raw visual values throughout components when a design token exists.

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

Preferred loop:

Page  
→ Implement  
→ Review  
→ Fix  
→ Freeze  
→ Next Page

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

---

# Phase 5 — Prototype Freeze

Once the frontend experience is approved, create a prototype checkpoint.

The prototype represents:

> What the product should do and how the user should experience it.

It does not represent the final engineering architecture.

After this checkpoint, export/eject the project from Base44.

---

# Phase 6 — Local Repository Becomes Source of Truth

After export/eject:

> Local Git repository = Source of Truth

Base44-generated architecture is treated as input, not as an unquestionable architectural foundation.

Base44 may still be used for isolated product/UI exploration, but production engineering decisions happen in the local repository.

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

User can view appointments end-to-end.

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

Appointment List  
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

Versioning guideline:

- Minor workflow refinements: `v0.2`, `v0.3`, etc.
- Stable initial workflow after sufficient real-world validation: `v1.0`
- Fundamental redesign after stabilization: future major version

Real project evidence has priority over preserving decisions from previous workflow versions.
