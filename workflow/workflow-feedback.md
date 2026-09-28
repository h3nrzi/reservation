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

The initial workflow effectively moves from Product Brief toward Page Inventory / Page Manifest and then Design Tokens / Base44 Foundation.

## Problem

A high-level Product Brief is insufficient for deciding which user steps deserve independent routes. Booking steps, management contexts, tabs, drawers, and modals can otherwise be mistaken for pages.

## Proposed Improvement

Product Brief  
→ Core User Journeys  
→ Capability Map  
→ Page Inventory Candidate  
→ Route / Screen Decisions  
→ Page Manifest  
→ Design Tokens  
→ Base44

## Expected Benefit

- Fewer premature route decisions
- Less confusion between steps and pages
- Better coverage of management capabilities
- More intentional UI architecture

## Validation Required

Evaluate the final Salon Booking Page Manifest against the original candidate inventory and assess whether the added discovery steps reduced ambiguity without excessive process.

---

# WF-002 — Explicit MVP Boundary Before Final Page Inventory

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project  
**Candidate Version:** v0.2

## Observation / Problem

Capability maps naturally contain both core and future capabilities. Without an explicit scope boundary, backlog features can silently become Base44 prototype requirements.

## Proposed Change

Product Brief  
→ Core User Journeys  
→ Capability Map  
→ MVP Boundary  
→ Page Inventory  
→ Route / Screen Decisions  
→ Page Manifest

## Expected Benefit

- Keeps Base44 focused on first-product scope
- Separates `not now` from `not part of the product`
- Reduces unnecessary page generation and later deletion

## Risks / Cost

Adds a discovery checkpoint and requires deliberate MVP decisions.

## Validation

Evaluate whether the Salon Booking MVP boundary produced a smaller, clearer Page Manifest without blocking obvious future evolution.

---

# WF-003 — Design Direction Before Design Tokens

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project  
**Candidate Version:** v0.2

## Observation / Problem

Design tokens should encode intentional visual decisions. Selecting colors, typography, radius, shadows, and density before agreeing on visual direction makes token values arbitrary implementation choices.

## Proposed Change

Page Manifest  
→ Design Direction  
→ Design Tokens  
→ Base44 Foundation Prompt

Design Direction should define visual personality, brand mood, customer/admin character, density, imagery role, typography/color direction, and surface philosophy without becoming a component-level specification.

## Expected Benefit

- Tokens become traceable to design intent
- Better customer/admin consistency
- Fewer arbitrary styling choices
- Clearer Base44 constraints

## Risks / Cost

An overly detailed direction phase could reduce useful design exploration.

## Validation

Apply `Warm Luxury` to the Salon Booking prototype and evaluate consistency and correction cycles.

---

# WF-004 — Separate Primitive, Semantic, and Component Tokens

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project  
**Candidate Version:** v0.2

## Current Behavior

The workflow requires Design Tokens but does not explicitly prescribe token layering.

## Observation / Problem

A generic instruction to create design tokens may produce only a raw palette. Generated components can then couple directly to primitive values such as `rose-700`, arbitrary hex values, or one-off Tailwind utilities.

That weakens themeability and makes future brand changes expensive because visual intent is distributed throughout application components.

## Proposed Change

Require Design Tokens to follow this dependency direction:

Primitive Tokens  
→ Semantic Tokens  
→ Component Usage / Variants  
→ UI

Example:

`rose-700`  
→ `primary`  
→ Primary Button  
→ Booking CTA

Application components should prefer semantic tokens whenever an appropriate semantic token exists.

## Expected Benefit

- Cleaner Tailwind/theme configuration
- Easier brand/theme changes
- Less arbitrary styling in generated code
- Better separation between palette and product meaning
- More consistent component states

## Risks / Cost

- Adds token-system structure to relatively small prototypes
- Too many semantic/component tokens could become unnecessary abstraction

The workflow should therefore require meaningful semantic layering without demanding exhaustive tokenization before evidence exists.

## Validation

During the Base44 foundation pass, inspect whether generated components use semantic styling consistently and whether raw hex/primitive values remain appropriately centralized.

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
