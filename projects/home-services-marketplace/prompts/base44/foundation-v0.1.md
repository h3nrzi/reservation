# Base44 Foundation Prompt — Home Services Marketplace

**Pass:** Foundation only

Create the frontend foundation for a Persian-first, RTL-native Home Services Marketplace POC. The product is a **request-and-quote marketplace**: a customer describes a household issue, providers submit comparable quotes, the customer chooses one, and the job status becomes visible. It is not an appointment-booking product.

## Scope for this pass

Create only:

1. Shared design tokens and typography.
2. Responsive Public, Customer Preview, Provider Preview, and focused Request Creation layouts.
3. Working navigation and identifiable **placeholder** pages for all routes below.
4. An explicit preview-role switch or navigation that makes it obvious there is no real authentication.
5. A small, deterministic set of fictional sample state sufficient to keep placeholder navigation coherent.

Do **not** fully design or implement any individual page in this pass. After the foundation is built, **STOP** and wait for a page-specific prompt.

## Routes

- `/` — Home, public placeholder
- `/categories` — category guidance placeholder
- `/request/new` — new request placeholder
- `/requests` — customer request list placeholder
- `/requests/:requestId` — customer request detail placeholder
- `/pro/requests` — provider request feed placeholder
- `/pro/requests/:requestId` — provider request detail and quote placeholder
- `/pro/jobs` — provider jobs placeholder

If your router uses a different notation for dynamic segments, use its equivalent. Unknown request IDs should reach a clear not-found state rather than crash.

## Product and locale rules

- All user-facing copy is natural Persian; the entire UI is RTL native. Keep technical route names and code symbols in English.
- Use Persian digits for visible counts/prices and `تومان` for price labels. Avoid catalog prices that imply a guaranteed service price; future provider quotes are estimates.
- Use fictional neighborhoods and sample users/providers only. Do not request or show real names, phone numbers, exact addresses, or payment data.
- There is no real provider matching, request delivery, quote submission, payment, live chat, upload, geolocation, database, backend, or authentication. Simulated states must be clearly understandable as preview data.
- The primary customer action is `درخواست خدمت`. Do not build a booking calendar or salon-style service selection flow.

## Design foundation — Practical Trust

Create a practical, calm marketplace visual language, clearly different from a luxury salon design. Use deep slate/navy text, warm off-white background, white panels, restrained teal for primary actions and progress, and amber only for urgency. Use Vazirmatn or a comparable Persian UI font. Keep mobile type readable and avoid oversized empty hero areas.

Organize tokens as **primitive values → semantic tokens → component usage**. Example primitive colors: slate `#0F172A`, `#334155`, `#64748B`; teal `#0F766E`, `#115E59`, `#CCFBF1`; amber `#B45309`, `#FEF3C7`; neutrals `#FFFFFF`, `#F8F7F3`, `#E2E8F0`; danger `#B91C1C`, `#FEE2E2`. Components should consume semantic tokens such as `background`, `surface`, `foreground`, `muted-foreground`, `primary`, `primary-foreground`, `border`, `success`, `warning`, `danger`, and `focus-ring` rather than scattering raw values.

Build basic button, form-field, status badge, and page-shell patterns only if the foundation needs them. Use visible keyboard focus and status text in addition to color. Make directional navigation correct for RTL without mirroring neutral icons.

## Foundation acceptance check

Before stopping, verify that every route opens, each layout is distinct but consistent, placeholder pages state their intended purpose, navigation works on narrow mobile and desktop, Persian copy is readable, and no full page was invented. Report any limitation or route that could not be created. Then **STOP**.
