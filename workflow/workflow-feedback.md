# Controlled Vibe Coding Workflow — Feedback Log

**Current Workflow Version:** v0.1  
**Status:** Active Evaluation

## Purpose

This document records problems, observations, successful patterns, and potential improvements discovered while applying the workflow to real projects.

Findings should not automatically modify the current workflow. They should provide evidence for future workflow versions.

---

# Feedback Statuses

Possible statuses:

- `Observed`
- `Under Evaluation`
- `Accepted for Next Version`
- `Rejected`
- `Resolved`

---

# WF-001 — Missing Discovery Layer Before Page Manifest

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project  
**Candidate Version:** v0.2

## Current v0.1 Assumption

The initial workflow effectively moves from:

Product Brief  
→ Page Inventory / Page Manifest  
→ Design Tokens  
→ Base44 Foundation

## Problem

During discovery for the salon booking project, it became clear that moving directly from a high-level Product Brief to a definitive Page Manifest is premature.

For example, a booking experience may conceptually contain:

- Select service
- Select specialist
- Select date
- Select time
- Enter details
- Review booking

These are distinct product steps but are not necessarily distinct pages/routes. They could instead be steps inside one route, components, modals, drawers, nested screens, or separate routes.

A simple page list does not contain enough product information to make that decision correctly. The same issue appeared when considering the management side of the salon application.

## Proposed Improvement

Introduce an explicit discovery layer:

Product Brief  
→ Core User Journeys  
→ Capability Map  
→ Page Inventory Candidate  
→ Route / Screen Decisions  
→ Page Manifest  
→ Design Tokens  
→ Base44

## Expected Benefit

This should reduce:

- Premature route decisions
- Artificially high page counts
- Confusion between user steps and application pages
- Missing management capabilities
- UI architecture decisions based on incomplete product understanding

## Validation Required

Continue the salon project using this expanded discovery process. After the Page Manifest is produced, evaluate whether the additional steps improved route decisions, reduced ambiguity, or added unnecessary process.

---

# WF-002 — Explicit MVP Boundary Before Final Page Inventory

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project  
**Candidate Version:** v0.2

## Current Behavior

The emerging discovery sequence identifies product capabilities and then moves toward page/screen definition.

## Observation / Problem

A capability map naturally includes both essential product capabilities and attractive future capabilities such as waitlists, loyalty, reviews, payments, promotions, memberships, gift cards, and reporting.

If page inventory is finalized directly from the full capability map, future capabilities can accidentally become part of the Base44 prototype. This increases page count, product complexity, and prototype scope before the core booking loop has been validated.

## Proposed Change

Add an explicit MVP boundary before final page inventory:

Product Brief  
→ Core User Journeys  
→ Capability Map  
→ MVP Boundary  
→ Page Inventory  
→ Route / Screen Decisions  
→ Page Manifest

## Expected Benefit

- Keeps Base44 focused on the first product scope.
- Prevents backlog capabilities from silently becoming prototype requirements.
- Makes page inventory easier to reason about.
- Creates a durable distinction between `not now` and `not part of the product`.
- Reduces wasted UI generation and later deletion.

## Risks / Cost

- Adds another explicit discovery checkpoint.
- Poor MVP decisions could prematurely exclude capabilities that materially affect UX architecture.

## Validation

Use the Salon Booking Project's MVP boundary to revise the candidate page inventory. Evaluate whether it produces a smaller, clearer, and more coherent Page Manifest without blocking obvious future evolution.

---

# WF-003 — Design Direction Before Design Tokens

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project  
**Candidate Version:** v0.2

## Current Behavior

The current workflow moves from Page Manifest directly to Design Tokens before the Base44 foundation pass.

## Observation / Problem

Design tokens should encode intentional visual decisions. If colors, typography, radius, shadows, density, and other tokens are selected without first agreeing on a visual/product direction, the token values become arbitrary implementation choices rather than a coherent design system.

The salon project exposed this when choosing between distinct directions such as warm luxury, modern minimal, and soft premium. Each direction could produce a valid but materially different token system.

## Proposed Change

Add an explicit Design Direction checkpoint before Design Tokens:

Page Manifest  
→ Design Direction  
→ Design Tokens  
→ Base44 Foundation Prompt

Design Direction should define enough intent to guide token creation, including where relevant:

- Visual personality
- Brand mood
- Customer-facing character
- Operational/admin character
- Density
- Photography/imagery role
- Typography direction
- Color direction
- Surface/border/shadow philosophy
- General interaction feel

It should avoid prematurely specifying every component or raw implementation value.

## Expected Benefit

- Makes design tokens traceable to explicit design intent.
- Reduces arbitrary color/radius/typography choices.
- Improves consistency between customer and admin surfaces.
- Gives Base44 clearer visual constraints before generation.
- Makes later design changes easier because the rationale exists above the token layer.

## Risks / Cost

- Adds another discovery/design checkpoint.
- An overly detailed Design Direction could become a premature design specification and reduce useful exploration.

## Validation

Apply the selected `Warm Luxury` direction to Design Tokens v0.1 for the Salon Booking Project. During Base44 generation, evaluate whether the direction materially improves consistency and reduces prompt correction cycles.

---

# Feedback Template

Future findings should use:

## WF-XXX — Title

**Status:** Observed  
**Discovered during:** Project  
**Candidate Version:** TBD

### Current Behavior

What does the workflow currently prescribe?

### Observation / Problem

What happened in practice?

### Proposed Change

What might improve the workflow?

### Expected Benefit

Why would the change help?

### Risks / Cost

What additional complexity could it introduce?

### Validation

How should we determine whether the change is actually better?
