# Base44 Page Prompt — Home

**Pass:** Implement `/` only

Using the existing approved Home Services Marketplace foundation, implement **only the Home page at `/`**. Preserve its Persian-first RTL behavior, Public layout, routes, Vazirmatn typography, Practical Trust visual direction, and semantic design tokens. Do not redesign the foundation or implement other placeholders. After Home is done, **STOP**.

## Page goal

A first-time visitor should quickly understand: describe a home problem → receive provider quotes → compare and choose → track the job. The main CTA is `درخواست خدمت` to `/request/new`. This is a marketplace; avoid booking slots, calendars, salon-like service cards, and fixed-price promises.

## Required structure

1. Compact hero with a concrete Persian promise, primary request CTA, and quieter category exploration link. Show the practical outcome above the fold on desktop and mobile.
2. Three-step process that explains request, quote comparison, and assignment/job progress in plain Persian.
3. Six useful categories: plumbing, electrical, appliance repair, HVAC, cleaning, and painting/handyman. Each category starts `/request/new` with that category selected if navigation state allows.
4. A clearly labeled **sample** request and two **fictional** quote summaries with consistent fields: estimate in Toman, included work, earliest broad availability, and provider trust signals. The two offers should differ meaningfully, so a comparison is useful.
5. Trust/process section: scope clarity, comparable offers, and transparent provider information. Do not claim real verification, insurance, or guarantees.
6. Concise FAQ: how price is decided, whether the system assigns a provider automatically, and what happens after a request is sent.
7. Final CTA and footer.

## Content and behavior

- Write credible, concise Persian copy. Avoid lorem ipsum, English UI text, fake live counts, and fabricated operational claims.
- Use fictional areas and providers. Any ratings or completed-job counts must be clearly example data.
- Make all links usable; pages that are not yet built remain intentional placeholders.
- Use restrained, coherent category icons and stable image fallbacks; do not depend on random remote images.
- Keep navigation, focus, buttons, and cards usable by keyboard and touch. Prevent horizontal overflow at narrow mobile widths.

## Completion report

When done, report what was implemented, which interactions work, and any unresolved issue. Do not continue to `/request/new` or any other page. **STOP**.
