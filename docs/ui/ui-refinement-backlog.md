# Salon Booking Platform — UI Refinement Backlog

**Status:** Active  
**Remediation Phase:** After Base44 prototype export, primarily with Codex/local codebase

## Purpose

Centralize visual, responsive, accessibility, asset, and component-quality issues discovered while reviewing Base44-generated pages.

During the Base44 phase, non-blocking issues are logged here rather than repeatedly spending generation cycles on polish.

After export, Codex should first look for systemic fixes at token/layout/component level, then resolve page-specific issues.

## Severity

- **Blocking** — page is unusable, structurally wrong, misleading, or cannot reasonably proceed.
- **High** — important quality/usability issue likely to affect multiple pages or core journeys.
- **Medium** — visible quality issue that should be fixed before production-quality UI.
- **Low** — optional polish.

## Scope

- **Global** — design system, tokens, typography, shared layout, asset policy.
- **Component** — reusable component or repeated pattern.
- **Page** — isolated page implementation.

---

# Home `/`

**Prototype status:** Product/structure approved  
**UI remediation status:** Deferred to local/Codex phase

| ID | Severity | Scope | Issue | Intended Direction |
|---|---|---|---|---|
| UI-HOME-001 | Medium | Page / Asset | One specialist portrait is broken/missing and renders as a placeholder. | Replace with a valid deterministic asset and ensure graceful fallback behavior. |
| UI-HOME-002 | Medium | Global / Asset | Specialist portraits are visually inconsistent in style, lighting, crop, and quality. | Establish an image/asset strategy and normalize aspect ratio, crop, quality, and visual character. |
| UI-HOME-003 | Medium | Global / Layout | Some sections use excessive vertical whitespace, weakening page rhythm and increasing unnecessary scroll length. | Audit section-gap usage and distinguish intentional editorial whitespace from accidental empty space. |
| UI-HOME-004 | Medium | Global / Typography | Some small supporting/orange text has weak readability and visual emphasis. | Review semantic muted/accent text colors, minimum text size, line-height, and contrast while preserving Warm Luxury. |
| UI-HOME-005 | Low | Global / Asset | Gallery and specialist imagery does not yet feel fully coherent as one brand image system. | Normalize image direction after export; define preferred photography style and reusable aspect-ratio rules. |

---

# Cross-Page Issues

Issues should move here when repeated on multiple pages or when review indicates that the correct fix belongs to the shared system rather than a single page.

| ID | Severity | Scope | Issue | Evidence | Intended Direction |
|---|---|---|---|---|---|
| UI-GLOBAL-001 | Medium | Global | No explicit production-ready visual asset strategy exists yet. | First observed on Home specialist/gallery imagery. | Define image categories, aspect ratios, crop rules, fallback behavior, and consistent visual direction before final UI polish. |

---

# Codex Remediation Order

After exporting the Base44 prototype to the local repository:

1. Audit architecture and generated component structure.
2. Identify repeated UI patterns and consolidate where appropriate.
3. Reconcile implementation with approved Design Tokens v0.2.
4. Fix Global backlog items first.
5. Fix reusable Component backlog items second.
6. Fix Page-specific backlog items third.
7. Run responsive QA across mobile, tablet, and desktop.
8. Run RTL/Persian typography and mixed-direction QA.
9. Run accessibility/contrast/focus QA.
10. Re-review all core journeys before backend integration.

## Rule

Do not blindly preserve Base44 implementation details when a cleaner reusable fix is available in the local codebase. Preserve approved product behavior and design intent, not accidental generated-code structure.

---

# Entry Template

| ID | Severity | Scope | Issue | Intended Direction |
|---|---|---|---|---|
| UI-PAGE-XXX | Medium | Page / Component / Global | Describe the observed issue. | Describe the desired direction without over-prescribing implementation. |
