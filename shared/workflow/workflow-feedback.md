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

Product Brief → Core User Journeys → Capability Map → Page Inventory Candidate → Route / Screen Decisions → Page Manifest → Design Tokens → Base44

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

Product Brief → Core User Journeys → Capability Map → MVP Boundary → Page Inventory → Route / Screen Decisions → Page Manifest

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

Page Manifest → Design Direction → Design Tokens → Base44 Foundation Prompt

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

Primitive Tokens → Semantic Tokens → Component Usage / Variants → UI

Application components should prefer semantic tokens whenever an appropriate semantic token exists.

## Expected Benefit

- Cleaner Tailwind/theme configuration
- Easier brand/theme changes
- Less arbitrary styling in generated code
- Better separation between palette and product meaning
- More consistent component states

## Risks / Cost

Adds token-system structure to relatively small prototypes. The workflow should require meaningful semantic layering without demanding exhaustive tokenization before evidence exists.

## Validation

During the Base44 foundation pass, inspect whether generated components use semantic styling consistently and whether raw hex/primitive values remain appropriately centralized.

---

# WF-005 — Locale & Market Requirements Early in Discovery

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project  
**Candidate Version:** v0.2

## Current Behavior

The workflow captures product goals, journeys, capabilities, pages, and design direction without an explicit early checkpoint for target language, writing direction, calendar, number formatting, currency, and other market-specific presentation requirements.

## Observation / Problem

The first Salon Booking Base44 foundation was generated successfully but in English/LTR because Persian-first requirements had never been made explicit. Locale affects typography, layout direction, navigation, steppers, sidebars, icons, calendars, dates, times, numbers, currency formatting, dummy data, and responsive behavior.

## Proposed Change

Add an explicit Locale & Market Requirements checkpoint near the beginning of discovery:

Product Brief → Locale & Market Requirements → Core User Journeys → Capability Map → MVP Boundary → Page Inventory → Route / Screen Decisions → Page Manifest → Design Direction → Design Tokens → Foundation Prompt

At minimum, decide or explicitly defer language, direction, typography/script, numerals, calendar, date/time formatting, currency, locale-specific dummy content, directional UI behavior, and i18n scope.

## Expected Benefit

- Prevents generating a structurally correct foundation for the wrong locale
- Makes typography decisions valid for the target script
- Surfaces RTL implications before layouts/components are generated
- Prevents calendar/currency/number assumptions from leaking into UI architecture
- Reduces avoidable regeneration and correction work

## Risks / Cost

Adds another early discovery checkpoint and can encourage premature internationalization. The checkpoint should distinguish locale requirements from full internationalization architecture.

## Validation

Regenerate the Salon Booking foundation from scratch using a Persian-first, RTL-native Foundation Prompt v0.2 and compare it with v0.1.

---

# WF-006 — Review UI Early, Defer Non-Blocking Refinement to Local/Codex

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Home Page  
**Candidate Version:** v0.2

## Current Behavior

The emerging page loop initially considered fixing UI issues inside Base44 before approving each page.

## Observation / Problem

The first generated Home page followed the approved product structure but exposed non-blocking UI issues such as inconsistent image quality, a broken specialist image, uneven portrait consistency, excessive vertical whitespace in places, and weak readability/contrast in some supporting copy.

These issues should be discovered early so they do not get forgotten. However, repeatedly spending Base44 generation cycles on visual polish can be expensive and inefficient when the project will later be exported and refined directly in code with Codex.

## Proposed Change

Separate **UI review** from **UI remediation**.

During Base44 prototype generation:

Page Spec → Page Prompt → Generate → Product/Structure Review → UI Review → Log UI Debt → Accept Prototype → Next Page

After prototype completion/export:

Export to Local → Codex Architecture Pass → UI Refinement Backlog → System/Component Fixes → Page-Specific Fixes → Responsive & Accessibility QA → Backend Integration

UI review remains mandatory during page generation, but non-blocking visual issues are logged instead of requiring another Base44 generation cycle.

Blocking issues that make a page unusable, structurally wrong, or misleading should still be corrected before moving on.

## Expected Benefit

- Detects visual debt while context is fresh
- Avoids paying repeated generation cost for polish that is cheaper to perform in code
- Produces one centralized, actionable refinement backlog for Codex
- Allows recurring problems to be fixed globally at component/token level after export
- Keeps Base44 focused on rapid product/UI prototyping
- Preserves a final dedicated responsive/accessibility quality pass

## Risks / Cost

- UI debt can accumulate if the backlog is vague or not maintained
- Later fixes may reveal that some issues should have been solved at foundation level
- Too much deferred work could make the exported prototype harder to normalize

The backlog therefore needs page, issue, severity, scope, and likely remediation level (global/component/page) so Codex can prioritize systemic fixes before one-off page fixes.

## Validation

Continue generating pages while logging UI debt. After export, measure whether Codex can resolve recurring issues centrally with fewer edits than repeated Base44 refinement would have required.

---

# WF-007 — Expiring Tool Budget Utilization

**Status:** Under Evaluation  
**Discovered during:** Salon Booking Project / Base44 Daily Credit Limit  
**Candidate Version:** v0.2

## Current Behavior

The workflow decides what to do next primarily from product/development sequence. It does not explicitly account for tools that have metered credits, daily quotas, temporary execution budgets, or other resources that expire/reset.

## Observation / Problem

Near the Base44 daily reset, a small amount of credit remained. Spending that remaining budget on a broad technical analysis produced less immediate value than using the same expiring budget for a bounded UI refinement pass based on already-known backlog items.

This suggests that tool constraints are part of workflow execution strategy. When a resource will expire anyway, the workflow can opportunistically use the remainder for useful, low-risk work without changing the main product plan.

## Proposed Change

Add a general **Expiring Resource Utilization Rule** for metered tools:

Primary Work  
→ Check Remaining Expiring Budget  
→ Select Useful Low-Risk Backlog Work  
→ Execute Only If It Fits the Remaining Budget  
→ Allow Quota/Window to Reset

Preferred uses of small expiring budgets, in order:

1. Small, already-understood backlog fixes
2. Low-risk UI polish / cleanup
3. Useful validation or QA
4. Independent tasks likely to complete within the remaining budget
5. Analysis only when that analysis is actually needed for an upcoming decision

Do not invent work merely to consume quota.

Do not use expiring budget as justification for:

- new unplanned features
- risky architecture changes
- broad refactors
- speculative analysis
- changes that cannot reasonably complete within the remaining budget

This rule should apply to any tool with non-rollover quotas/credits or reset windows, not only Base44.

If unused quota rolls over, consumption creates additional cost, or the remaining budget has future value, do not spend it merely for utilization.

## Expected Benefit

- Extracts useful value from otherwise expiring tool capacity
- Reduces waste in quota-limited workflows
- Encourages bounded tasks that match the available execution budget
- Can reduce later cleanup cost without disrupting the primary development sequence
- Makes tool economics an explicit workflow concern

## Risks / Cost

- Can encourage unnecessary work if interpreted as "always use every credit"
- Small-budget tasks can accidentally expand in scope
- Opportunistic changes can distract from the main workflow if not backlog-driven

The rule must therefore require useful, known, low-risk work and treat unused quota as acceptable when no suitable task exists.

## Validation

Apply the rule across future Base44 reset cycles and other metered tools. Evaluate whether leftover budget consistently produces useful completed work without creating rework, scope creep, or additional paid usage.

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
