# Controlled Vibe Coding Workflow — Feedback Log

**Current Workflow Version:** v0.1  
**Status:** Active Evaluation

## Purpose

This document records problems, observations, successful patterns, and potential improvements discovered while applying the workflow to real projects.

Findings should not automatically modify the current workflow.

They should provide evidence for future workflow versions.

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

These are distinct product steps but are not necessarily distinct pages/routes.

They could instead be:

- Steps inside one route
- Components inside a booking flow
- Modals
- Drawers
- Nested screens
- Separate routes

A simple page list does not contain enough product information to make that decision correctly.

The same issue appeared when considering the management side of the salon application.

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

Continue the salon project using this expanded discovery process.

After the Page Manifest is produced, evaluate whether the additional steps:

- improved route decisions
- reduced ambiguity
- added unnecessary process
- should become mandatory in v0.2

Do not mark this change as accepted until tested further.

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
