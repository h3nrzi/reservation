# IT Support Desk — Design Direction

**Version:** 0.1

**Status:** Proposed for the first frontend POC

## Character

A calm, dependable workspace for reporting and resolving IT issues in a small company. Employees should feel heard and know what happens next. Agents should scan and act quickly. Managers should notice risk without hunting through charts.

## Visual priorities

- Lead with subject, current status, owner, last update, and next action on ticket surfaces.
- Use a compact, scannable team queue and a more comfortable, guided requester form.
- Give SLA risk and priority distinct labels as well as colors; avoid making red the default visual language.
- Use restrained neutral surfaces, a clear primary action color, and semantic status colors. Exact values belong in later design tokens.
- Keep the conversation chronological and distinguish requester, agent, and system activity.
- Prefer readable typography, clear borders, and spacing over decorative illustrations, large shadows, or many nested cards.

## Interaction and accessibility

Keep filters visible in queue context and preserve ticket context when opening detail. Show state changes immediately in the demo, with clear validation and blocked-action feedback. Support keyboard focus, readable contrast, mobile form use, and responsive table alternatives. Status meaning must remain clear without color.

The application direction, typeface, numeral, and date/time presentation follow the separate locale decision. Directional placement and icons must work in that chosen writing direction. No customer-marketing layout is needed for this internal tool.

## Base44 handoff

Use this direction to derive a small token set and the two layout families in the [proposed page manifest](../product/page-manifest.md). The foundation pass creates placeholders and shared styling only, then stops for review. Detailed ticket pages follow one at a time with deterministic dummy data.
