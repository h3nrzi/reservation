# Salon Booking Platform — Design Tokens

**Version:** 0.1  
**Status:** Approved Design Baseline  
**Design Direction:** Warm Luxury

## Purpose

Translate `design-direction-v0.1.md` into concrete, reusable design values suitable for the frontend foundation and Tailwind configuration.

Token architecture:

Primitive Tokens  
→ Semantic Tokens  
→ Component Usage / Variants  
→ Tailwind / UI Implementation

Components should prefer semantic tokens rather than directly coupling themselves to primitive palette values.

---

# 1. Primitive Colors

## Warm Neutral

| Token | Value |
|---|---|
| warm-50 | `#FCFAF7` |
| warm-100 | `#F7F2EC` |
| warm-200 | `#EDE4DA` |
| warm-300 | `#DDCFC1` |
| warm-400 | `#BDAA98` |
| warm-500 | `#9B8775` |
| warm-600 | `#796757` |
| warm-700 | `#5E4E41` |
| warm-800 | `#44372F` |
| warm-900 | `#2E2520` |
| warm-950 | `#1D1714` |

## Muted Rose

| Token | Value |
|---|---|
| rose-50 | `#FCF7F7` |
| rose-100 | `#F8EEEE` |
| rose-200 | `#EFDADA` |
| rose-300 | `#E1BCBE` |
| rose-400 | `#CD969B` |
| rose-500 | `#B8757D` |
| rose-600 | `#9E5963` |
| rose-700 | `#83464F` |
| rose-800 | `#6D3C44` |
| rose-900 | `#5C353C` |
| rose-950 | `#321A1F` |

Muted Rose is the restrained brand accent. It must not make the application predominantly pink.

---

# 2. Semantic Colors

| Semantic Token | Initial Mapping |
|---|---|
| background | `warm-50` |
| foreground | `warm-950` |
| surface | `#FFFFFF` |
| surface-subtle | `warm-100` |
| surface-elevated | `#FFFFFF` |
| primary | `rose-700` |
| primary-hover | `rose-800` |
| primary-foreground | `#FFFFFF` |
| secondary | `warm-200` |
| secondary-foreground | `warm-900` |
| muted | `warm-100` |
| muted-foreground | `warm-600` |
| border | `warm-200` |
| border-strong | `warm-300` |
| input | `warm-200` |
| ring | `rose-500` |

## Feedback Colors

The system must define independent accessible semantic colors for:

- success
- success-foreground
- warning
- warning-foreground
- danger
- danger-foreground
- info
- info-foreground

These should not reuse the brand Rose merely because it is available. Exact accessible values may be finalized during implementation/contrast validation.

---

# 3. Typography Families

## Display

`Cormorant Garamond`

Use selectively for customer-facing editorial moments:

- Hero headings
- Major section headings
- Selected marketing/editorial headings

Do not use for forms, buttons, tables, booking controls, or routine admin UI.

## Sans

`Inter`

Primary functional typeface for:

- Body text
- Navigation
- Forms
- Buttons
- Booking controls
- Tables
- Admin interface
- Labels and metadata

---

# 4. Type Scale

| Token | Size |
|---|---:|
| text-xs | 12px |
| text-sm | 14px |
| text-base | 16px |
| text-lg | 18px |
| text-xl | 20px |
| text-2xl | 24px |
| text-3xl | 30px |
| text-4xl | 36px |
| text-5xl | 48px |
| text-6xl | 60px |

Customer editorial/hero contexts may use the upper end of the scale.

Admin UI should generally remain within `text-sm` through `text-2xl`, except where a stronger hierarchy is justified.

Exact font weights and line heights should follow readable defaults and may be refined during foundation validation.

---

# 5. Radius

| Token | Value |
|---|---:|
| radius-sm | 6px |
| radius-md | 10px |
| radius-lg | 16px |
| radius-xl | 24px |
| radius-full | 9999px |

Initial component guidance:

- Button → `radius-md`
- Input/control → `radius-md`
- Card → `radius-lg`
- Modal → `radius-lg` or `radius-xl`
- Badge → `radius-full`

`radius-full` should only be used where a pill/circle shape has semantic or interaction value. Avoid generic rounded-pill styling everywhere.

---

# 6. Shadows

Keep a restrained three-level shadow vocabulary:

- `shadow-sm`
- `shadow-md`
- `shadow-lg`

Principle:

> Prefer whitespace and subtle borders before adding shadow.

Typical usage:

- Dropdown / Popover → `shadow-md`
- Drawer / Modal → `shadow-md` or `shadow-lg`
- Ordinary content cards → usually border/no shadow or at most `shadow-sm` when justified

Avoid floating-card aesthetics across the entire interface.

---

# 7. Spacing Policy

Retain the standard Tailwind spacing scale unless real product needs justify a change.

Do not create a parallel arbitrary spacing system.

Semantic layout tokens:

| Token | Value |
|---|---:|
| page-gutter-mobile | 16px |
| page-gutter-tablet | 24px |
| page-gutter-desktop | 32px |
| section-gap-mobile | 64px |
| section-gap-desktop | 96px |
| content-max | 1280px |
| reading-max | 720px |

Customer discovery pages may use full-width imagery/sections while keeping textual content aligned to appropriate containers.

---

# 8. Layout Tokens

## Admin

| Token | Value |
|---|---:|
| admin-sidebar-width | 256px |
| admin-header-height | 64px |
| admin-content-max | fluid / no fixed maximum where operationally useful |

Calendar and data-heavy management experiences should make effective use of desktop viewport width.

## Customer

Default content maximum:

`1280px`

Focused reading/content contexts may use `reading-max`.

---

# 9. Control Heights & Density

| Token | Value |
|---|---:|
| control-sm | 36px |
| control-md | 44px |
| control-lg | 52px |

Guidance:

- Customer → primarily `control-md` / `control-lg`
- Booking → primarily `control-md` / `control-lg`
- Admin → primarily `control-sm` / `control-md`

This allows customer and admin surfaces to share a design system while intentionally using different density levels.

---

# 10. Responsive Policy

Use standard Tailwind breakpoints initially:

- `sm`
- `md`
- `lg`
- `xl`
- `2xl`

Do not introduce custom breakpoints unless prototype evidence shows a real need.

Principles:

- Customer experiences are designed mobile-first.
- Desktop must not look like a merely enlarged mobile layout.
- Admin/calendar experiences require explicit desktop usability consideration.
- Responsive behavior should preserve task clarity rather than simply stacking every element.

---

# 11. Interaction State Vocabulary

Interactive components must account for:

- default
- hover
- active
- focus
- disabled
- selected
- loading

Initial focus guidance:

- focus ring: 2px
- focus offset: 2px
- focus color: semantic `ring`

Focus indication must remain visible and accessible.

---

# 12. Accessibility

Design-token implementation must preserve:

- Sufficient text/background contrast
- Readable muted text
- Visible keyboard focus
- Adequate touch/click targets
- Non-color-only status communication
- Readable responsive typography

Exact semantic feedback colors should be validated for contrast during implementation rather than selected solely for aesthetic fit.

---

# 13. Dark Mode

Dark mode is intentionally outside Design Tokens v0.1 scope.

The semantic-token architecture should avoid making a future second theme unnecessarily difficult, but Base44 should not implement dark mode during the initial prototype.

---

# 14. Tailwind Implementation Rules

The frontend styling foundation should:

1. Preserve useful Tailwind defaults where no project-specific decision exists.
2. Expose the approved palette/tokens through the project's styling configuration or CSS variable strategy as appropriate to the generated stack.
3. Prefer semantic classes/tokens in application components.
4. Avoid scattering raw hex values across components.
5. Avoid direct primitive palette coupling when a semantic token exists.
6. Avoid arbitrary values when an approved token or standard scale value is appropriate.
7. Support customer, booking, and admin density differences through deliberate component sizing/variants rather than unrelated component systems.

---

# 15. Token Architecture Rule

Preferred dependency direction:

Primitive Tokens  
→ Semantic Tokens  
→ Component Variants  
→ UI

Example:

`rose-700`  
→ `primary`  
→ primary Button  
→ Booking CTA

Avoid:

Booking CTA  
→ hard-coded `#83464F`

This separation is required so future brand/theme changes can be made without rewriting component styling across the application.

---

# Validation During Base44 Foundation

Evaluate:

- Whether Base44 actually uses the token system instead of arbitrary styling
- Whether customer and admin surfaces feel related but appropriately different in density
- Whether typography feels premium without harming usability
- Whether Muted Rose remains an accent rather than dominating the interface
- Whether cards, pills, gradients, and shadows remain restrained
- Whether generated responsive behavior follows the intended layout philosophy

Corrections discovered during the foundation pass should inform both project documentation and workflow feedback where applicable.

---

# Next Step

Design Tokens v0.1  
→ Base44 Foundation Prompt #1  
→ Generate Routes + Layouts + Placeholders + Styling Foundation  
→ STOP  
→ Foundation Review
