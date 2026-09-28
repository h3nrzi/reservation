# Salon Booking Platform — Design Tokens

**Version:** 0.2  
**Status:** Approved Design Baseline  
**Design Direction:** Warm Luxury  
**Locale Baseline:** Persian-first / RTL-native

## Purpose

Define the current standalone visual and locale token system for the Persian-first Salon Booking prototype. This document is the source of truth for the approved foundation.

Token architecture:

Primitive Tokens  
→ Semantic Tokens  
→ Component Usage / Variants  
→ Tailwind / UI Implementation

---

# 1. Primitive Colors

Use these primitive colors centrally.

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

Muted Rose remains a restrained accent, not the dominant application color.

---

# 2. Semantic Colors

Map application colors through these semantic tokens:

| Semantic Token | Mapping |
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

Define independent accessible semantic feedback colors for success, warning, danger, and info.

---

# 3. Persian Typography

## Primary Typeface

`Vazirmatn`

Vazirmatn is the primary typeface for Persian customer, booking, and admin UI.

Do not rely on Latin display typography for Persian user-facing content.

Use typography hierarchy, scale, weight, whitespace, composition, and imagery to create the premium/editorial character rather than forcing a Latin display typeface into Persian UI.

Recommended initial roles:

- Hero / major customer heading → Vazirmatn, strong scale, deliberate weight
- Section headings → Vazirmatn
- Body → Vazirmatn
- Forms / buttons / controls → Vazirmatn
- Admin → Vazirmatn
- Tables / labels / metadata → Vazirmatn

Latin fragments may use a sensible Latin fallback where necessary.

Do not introduce a second Persian display font in Foundation v0.2 without explicit approval.

---

# 4. Type Scale

Use this initial type scale:

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

Persian line-height and font-weight choices must be validated visually rather than copied blindly from Latin typography assumptions.

Avoid overly tight line-height for Persian text.

Admin UI should generally remain within `text-sm` through `text-2xl`.

---

# 5. Direction Tokens / Logical Layout Policy

The application is RTL-native.

Where the generated stack supports it, prefer logical layout concepts over physical left/right assumptions:

- start / end
- inline-start / inline-end
- margin/padding logical equivalents
- border-start / border-end
- start/end alignment

The root Persian application experience should use RTL direction semantics.

Do not implement RTL merely through `text-align: right`.

Directional components must account for RTL semantics, including:

- navigation
- breadcrumb separators
- chevrons/arrows
- previous/next controls
- booking progress/stepper
- pagination
- drawers
- sidebar placement
- calendar navigation

Non-directional icons should not be mirrored unnecessarily.

---

# 6. Numeral Presentation

Default user-facing presentation uses Persian digits.

Examples:

- `۱۲`
- `۱۴۰۵`
- `۱۷:۳۰`
- `۱٬۲۵۰٬۰۰۰ تومان`

Presentation formatting must remain separate from future stored/domain values.

Inputs such as phone numbers and mixed-direction identifiers require deliberate handling and must not be blindly transformed in a way that harms entry or machine processing.

---

# 7. Date, Time & Money Presentation

## Calendar

Customer-facing and admin-facing calendar presentation is Jalali / Solar Hijri.

Do not encode a backend storage strategy into the design-token layer.

## Time

Use 24-hour presentation.

Example: `۱۷:۳۰`

## Currency

Use Toman for customer-facing price presentation.

Example: `۱٬۲۵۰٬۰۰۰ تومان`

Formatting should eventually be centralized through locale-aware utilities rather than duplicated across components.

---

# 8. Radius

Use these radius tokens:

| Token | Value |
|---|---:|
| radius-sm | 6px |
| radius-md | 10px |
| radius-lg | 16px |
| radius-xl | 24px |
| radius-full | 9999px |

Usage guidance:

- Button → `radius-md`
- Input/control → `radius-md`
- Card → `radius-lg`
- Modal → `radius-lg` or `radius-xl`
- Badge → `radius-full`

Avoid pill styling everywhere.

---

# 9. Shadows

Use a restrained `shadow-sm`, `shadow-md`, and `shadow-lg` vocabulary.

Prefer whitespace and subtle borders before shadows.

Elevated shadows belong primarily to popovers, dropdowns, drawers, and modals.

---

# 10. Spacing & Layout

Standard Tailwind spacing remains preferred unless evidence requires changes.

| Token | Value |
|---|---:|
| page-gutter-mobile | 16px |
| page-gutter-tablet | 24px |
| page-gutter-desktop | 32px |
| section-gap-mobile | 64px |
| section-gap-desktop | 96px |
| content-max | 1280px |
| reading-max | 720px |

RTL does not change these spacing magnitudes; it changes directional application where relevant.

---

# 11. Layout Tokens

## Admin

| Token | Value |
|---|---:|
| admin-sidebar-width | 256px |
| admin-header-height | 64px |
| admin-content-max | fluid where operationally useful |

For Persian RTL desktop admin, the primary sidebar should be positioned on the **right**.

## Customer

Default content max remains `1280px`.

Full-width imagery/sections remain allowed where appropriate.

---

# 12. Control Heights & Density

Use these control-height tokens:

| Token | Value |
|---|---:|
| control-sm | 36px |
| control-md | 44px |
| control-lg | 52px |

Guidance:

- Customer → `control-md` / `control-lg`
- Booking → `control-md` / `control-lg`
- Admin → `control-sm` / `control-md`

Validate Persian labels against control widths; do not assume English text lengths.

---

# 13. Responsive Policy

Retain standard Tailwind breakpoints initially:

- `sm`
- `md`
- `lg`
- `xl`
- `2xl`

Customer remains mobile-first.

Admin remains explicitly desktop-aware.

Responsive implementation must be tested with real Persian text because wrapping and label lengths differ from English.

RTL navigation behavior must remain correct at all breakpoints.

---

# 14. Interaction States

All interactive components must support:

- default
- hover
- active
- focus
- disabled
- selected
- loading

Focus guidance remains:

- ring → 2px
- offset → 2px
- color → semantic `ring`

Keyboard/focus order must remain logical in RTL layouts.

---

# 15. Mixed-Direction Content

RTL components must safely support embedded LTR fragments such as:

- phone numbers
- URLs
- email addresses
- IDs
- technical codes

Use bidi-aware implementation where required rather than relying on accidental browser rendering.

---

# 16. Accessibility

The implementation must preserve:

- sufficient text/background contrast
- readable muted text
- visible keyboard focus
- adequate touch and click targets
- status meaning beyond color alone
- responsive typography
- Persian text readability
- adequate Persian line height
- logical RTL keyboard/focus flow
- understandable directional icons
- readable mixed RTL/LTR content
- clear numeral/input behavior

Premium styling must never depend on low contrast.

---

# 17. Dark Mode

Dark mode is outside the current prototype scope.

Do not implement dark mode in Foundation v0.2.

---

# 18. Tailwind / Styling Implementation Rules

1. Preserve useful Tailwind defaults where no project decision exists.
2. Centralize approved primitive and semantic tokens.
3. Prefer semantic tokens in components.
4. Avoid scattered raw hex values.
5. Avoid primitive coupling where semantic meaning exists.
6. Prefer logical direction-aware styling over unnecessary `left`/`right` assumptions.
7. Establish RTL at the application/layout level, not through ad-hoc per-component fixes.
8. Support density variants without separate unrelated design systems.
9. Do not add a language switcher or full translation framework solely because the app is Persian-first.
10. Keep technical routes and engineering identifiers in English.

---

# 19. Token Architecture Rule

Preferred dependency direction:

Primitive Tokens  
→ Semantic Tokens  
→ Component Variants  
→ UI

Locale presentation concerns should similarly be centralized rather than scattered:

Locale Requirements  
→ Formatting / Direction Rules  
→ Components  
→ UI

Avoid page-level one-off Persian/RTL hacks.

---

# 20. Foundation v0.2 Validation

Evaluate whether Base44:

- establishes true RTL direction rather than right-aligned LTR
- uses Vazirmatn consistently
- renders representative Persian UI copy naturally
- uses Persian digits in representative display content
- positions the admin sidebar on the right
- handles directional icons correctly
- preserves Warm Luxury without Latin-only typography
- keeps the existing palette restrained
- demonstrates Jalali-aware date/calendar direction
- demonstrates Toman-aware price presentation
- demonstrates 24-hour time
- avoids unnecessary full-i18n infrastructure
- preserves all 23 approved routes

---
