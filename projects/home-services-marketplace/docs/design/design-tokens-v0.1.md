# Design Tokens — Practical Trust

**Version:** 0.1

**Status:** Foundation specification; verify contrast in generated UI

## Primitive layer

| Family | Values | Use |
| --- | --- | --- |
| Slate | `#0F172A`, `#334155`, `#64748B` | Text and deep surfaces |
| Teal | `#0F766E`, `#115E59`, `#CCFBF1` | Action and success/progress |
| Amber | `#B45309`, `#FEF3C7` | Caution and urgency only |
| Neutral | `#FFFFFF`, `#F8F7F3`, `#E2E8F0` | Cards, background, borders |
| Danger | `#B91C1C`, `#FEE2E2` | Errors and destructive states |

## Semantic layer

| Token | Intent |
| --- | --- |
| `background` | Warm neutral page canvas |
| `surface` | White card or panel |
| `foreground` | Deep slate primary text |
| `muted-foreground` | Secondary copy with readable contrast |
| `primary` / `primary-foreground` | Teal action and legible text on it |
| `border` | Quiet boundaries between fields and cards |
| `success`, `warning`, `danger` | Meaningful state colors, always paired with text |
| `focus-ring` | Visible keyboard focus across light/dark surfaces |

## Component usage

- Primary button: one dominant action per section; secondary and text styles for alternatives.
- Status badge: named request/quote/job state plus color, never color alone.
- Quote card: fixed information order; selected state uses border, label, and icon rather than color alone.
- Form field: persistent label, hint or error text, and adequate touch target.
- Stepper: numbered Persian labels with current/completed states that work in RTL.

Use primitive values only in the central theme/token configuration. Components consume semantic tokens. Keep Tailwind's normal spacing scale unless a documented product need requires a custom value. Define a restrained radius and shadow scale instead of per-card one-offs.

## Accessibility checks

Verify text/background contrast in the rendered pages, focus visibility, status meaning without color, readable mobile type, and mixed-direction numbers/IDs. Token values are a starting point, not a claim of verified contrast in every combination.
