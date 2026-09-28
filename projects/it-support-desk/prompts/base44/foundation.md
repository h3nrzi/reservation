# Base44 Foundation Prompt — IT Support Desk

**Prompt version:** 0.1

**Status:** Prepared draft for the user to run after reviewing the locale defaults and proposed route/design decisions. No Base44 output has been reviewed.

Build the **foundation only** for a Persian, RTL-native internal IT Support Desk for a small company. Employees report and follow IT tickets; support agents triage, assign, reply, and resolve; a manager sees queue and SLA risk. The later POC will use deterministic dummy data. Do not implement the ticket journeys in this pass.

## Exact scope

Create exactly these five routes with navigable, minimal Persian placeholders:

1. `/my/tickets` — تیکت‌های من (requester list)
2. `/my/tickets/new` — ثبت تیکت (requester form placeholder)
3. `/tickets/:ticketId` — جزئیات تیکت (shared detail placeholder)
4. `/agent/queue` — صف پشتیبانی (agent queue placeholder)
5. `/manager/overview` — نمای مدیر (manager overview placeholder)

Use two related layout families: a comfortable requester workspace and a denser internal operations workspace. The shared ticket detail changes visible actions by demo role later; do not create separate detail routes. Include a visible **demo role switch** in the shell so all three perspectives can be inspected. It is only a prototype control, not login, authentication, or authorization. No landing, login, settings, or extra product routes.

Each placeholder needs only its page title, layout, a short description, and links that verify navigation. A minimal example ticket link may point to `/tickets/T-1001`; do not build a full dataset, form, queue, conversation, dashboard, or status workflow in this foundation pass.

## Locale and direction

- All visible copy must be natural Persian. Build native RTL at the application/layout level, not an LTR layout with right-aligned text.
- Use Vazirmatn for UI. Keep technical route paths and implementation identifiers in English.
- Assume fa-IR, Asia/Tehran, Jalali display dates, 24-hour time, and Persian digits for ordinary UI samples. A representative date/time sample is enough for this pass.
- Keep ticket IDs, email, URLs, and other technical fragments in LTR order within RTL layouts. Do not reverse characters.
- Put desktop operations navigation on the right. Mirror directional controls when their meaning requires it. Keep keyboard order logical.
- Do not add a language switcher or translation-management system.

## Visual foundation

Aim for a calm, dependable work tool: clear hierarchy, readable status labels, compact queue navigation, and a comfortable requester form. Establish reusable primitive and semantic tokens with these starting values: page `#F6F8FB`, surface `#FFFFFF`, foreground `#172536`, muted foreground `#526274`, border `#D5DEE8`, primary `#174A7E`, primary foreground `#FFFFFF`, success `#176B50`, warning `#9B5A12`, danger `#B33535`, and focus ring `#2D77B8`. Components should use semantic tokens rather than isolated raw colors. Use Vazirmatn, a 16px body baseline, 40–44px controls, an 8px spacing rhythm, restrained 8px radius, visible focus, and readable contrast. Avoid decorative illustrations, heavy gradients/shadows, and card nesting.

Make shells responsive. On narrow screens, navigation must remain usable, labels must not be clipped, and the eventual queue should have room for a stacked-row alternative. Build only the foundation needed to validate this direction now.

## Data and behavior boundary

The later page passes will use fictional, deterministic tickets. For now, use only the minimal static placeholder content needed to verify routes, role perspectives, direction, and layout. No backend, database, API, remote persistence, real authentication, notifications, attachments, SLA engine, or integrations. Do not infer finished product behavior from placeholder links.

## Acceptance check and stop point

Before stopping, verify that all five routes render, role switching exposes the appropriate navigation shell, Persian text and mixed LTR IDs display correctly, the operations navigation sits on the right on desktop, responsive navigation is usable, and focus is visible. Keep page content as placeholders. Report what was created and any unresolved issues, then **STOP**. Do not continue to detailed ticket pages or add routes.
