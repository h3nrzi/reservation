# IT Support Desk — Initial Design Tokens

**Version:** 0.1

**Status:** Proposed foundation values; validate against rendered pages

These values translate the [design direction](design-direction.md) into a restrained starting system. Use semantic tokens in UI components rather than scattering raw colors. Adjust values only after reviewing the rendered foundation and checking contrast.

| Token | Starting value | Use |
| --- | --- | --- |
| Page background | `#F6F8FB` | Quiet workspace canvas |
| Surface | `#FFFFFF` | Forms, queue and detail panels |
| Foreground | `#172536` | Primary text |
| Muted foreground | `#526274` | Secondary text; check small-text contrast |
| Border | `#D5DEE8` | Dividers and input boundaries |
| Primary | `#174A7E` | Main action and active navigation |
| Primary foreground | `#FFFFFF` | Text on primary |
| Success | `#176B50` | Resolved/closed meaning |
| Warning | `#9B5A12` | At-risk meaning |
| Danger | `#B33535` | Overdue/error meaning |
| Focus ring | `#2D77B8` | Visible keyboard focus |

Use Vazirmatn for headings, body, and controls. Start with a compact but readable operations density: 16px body text, generous line height for Persian messages, 40–44px controls, 8px spacing rhythm, 8px default radius, and subtle or no shadow. The requester form may have more breathing room than the agent queue. Preserve readable contrast in semantic badges and never rely on color alone for state.

Use a right-side desktop operations navigation for RTL. On narrow screens, replace wide tables with readable stacked rows and keep the primary action reachable. The Base44 foundation should establish these tokens and layout rules, not produce finished ticket pages.
