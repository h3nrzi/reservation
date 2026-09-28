# Salon Booking Platform — Services Page Spec

**Version:** 0.1  
**Status:** Approved for Page Prompt Drafting  
**Route:** `/services`  
**Surface:** Customer / Public  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

## Purpose

Define the product, information architecture, content, interactions, and responsive intent for the Services listing page before Base44 implementation.

This page is a discovery and decision surface. It should help users understand available beauty services, compare relevant options, and move naturally toward a service detail or booking flow.

---

# 1. Primary Goal

Help visitors answer three questions efficiently:

1. چه خدماتی ارائه می‌شود؟
2. کدام خدمت برای نیاز من مناسب‌تر است؟
3. چطور جزئیات را ببینم یا برای آن نوبت رزرو کنم؟

Primary actions:

- View service details → `/services/:serviceId`
- Begin booking → `/book`

The page should support discovery without becoming a dense e-commerce catalog.

---

# 2. Page Roles

The Services page primarily supports:

- **Discovery** — understand the salon's service offering.
- **Comparison** — distinguish categories/services using useful information.
- **Decision** — open the relevant service detail.
- **Conversion** — begin booking when the user is ready.

Do not overload the listing with every detail that belongs on the Service Detail page.

---

# 3. Information Architecture

Recommended structure:

1. Public Header
2. Services Intro / Page Hero
3. Service Category Navigation / Filter
4. Services Listing
5. Booking Guidance / Contextual CTA
6. Final Booking CTA
7. Public Footer

Keep the page focused. Do not add unrelated marketing sections already covered by Home.

---

# 4. Services Intro

Create a concise page introduction.

The user should immediately understand that services can be explored before booking and that details such as duration, pricing direction, and relevant specialists can be discovered deeper in the flow.

Use natural Persian copy.

Avoid oversized marketing hero treatment that pushes the actual service list too far below the fold.

A small editorial image or restrained visual composition is acceptable, but service discovery must remain the priority.

---

# 5. Service Taxonomy

Use a small deterministic taxonomy appropriate for the prototype.

Suggested categories:

- مو
- میکاپ
- ناخن
- ابرو و مژه
- مراقبت و زیبایی

Representative services may include:

- رنگ و لایت
- بالیاژ
- کوتاهی و استایل مو
- براشینگ
- میکاپ
- میکاپ عروس
- مانیکور
- پدیکور
- ژلیش ناخن
- اصلاح و طراحی ابرو
- لیفت و لمینت مژه
- تراپی و مراقبت مو

This taxonomy is prototype content, not a final production catalog.

Use stable IDs/slugs in dummy data so listing items can route consistently to service detail placeholders.

---

# 6. Category Navigation / Filtering

Provide a simple way to browse services by category.

This may be implemented as an RTL-friendly category filter/tab/chip pattern, but avoid excessive pill styling.

Include an `همه خدمات` state.

Requirements:

- clearly show the selected category
- remain usable on mobile
- avoid horizontal overflow that makes categories difficult to discover
- preserve keyboard accessibility
- do not introduce complex faceted search/filter infrastructure

A full search system is not required for v0.1 unless it is genuinely useful and remains simple.

---

# 7. Service Listing

Show enough deterministic services to make category browsing meaningful, approximately **8–12 items** across the taxonomy.

Each service preview should prioritize decision-useful information.

Recommended fields:

- service name
- category
- short Persian description
- representative duration or duration range
- representative starting price or price range
- relevant image where it adds value
- action to view details
- optional direct booking action where composition remains clear

Example price presentation:

`از ۱٬۲۵۰٬۰۰۰ تومان`

Example duration:

`حدود ۹۰ دقیقه`

Do not fabricate discounts, ratings, popularity badges, scarcity, or "best seller" labels.

Do not overload cards with specialist lists, full descriptions, policies, preparation instructions, or detailed pricing breakdowns; those belong deeper in the experience.

---

# 8. Service Card / Item Behavior

The service item should make the primary next step obvious.

Preferred hierarchy:

1. Understand the service
2. See key duration/price context
3. Open details
4. Book when ready

Service detail route:

`/services/:serviceId`

Booking route:

`/book`

If booking is initiated from a service item, the future implementation should be able to preserve the selected service context. During Base44 prototype generation, do not build real state persistence or backend logic solely for this.

Avoid making the entire card interaction ambiguous when it also contains multiple actions.

---

# 9. Pricing Communication

Prices are representative prototype data.

Use Toman and Persian digits.

When exact final price depends on factors not yet modeled, prefer honest language such as:

- `از ... تومان`
- `بازه قیمت ...`

Do not imply that every beauty service necessarily has one fixed final price.

Do not introduce discounts/promotional pricing without product requirements.

---

# 10. Duration Communication

Show duration only where it helps booking expectations.

Use concise Persian formatting such as:

- `حدود ۶۰ دقیقه`
- `۹۰ تا ۱۲۰ دقیقه`

Do not imply operational precision that the prototype does not actually support.

---

# 11. Booking Guidance

Include a concise contextual area explaining that after choosing a service, the user can continue to select a suitable specialist and appointment time.

This should reduce uncertainty rather than repeat the full booking tutorial from Home.

Possible CTA:

**شروع رزرو** → `/book`

Do not duplicate the complete `/book` flow.

---

# 12. Final Booking CTA

Provide a clear conversion opportunity after browsing.

Primary action:

**رزرو نوبت** → `/book`

The CTA should feel consistent with Home and the Public Layout rather than becoming a new visual pattern.

---

# 13. Dummy Data Policy

Create deterministic Persian service data reusable by later pages.

Prefer a shared mock-data structure containing fields conceptually similar to:

- id
- slug
- name
- category
- shortDescription
- duration
- priceFrom / priceRange
- image

Do not over-engineer a production domain model during Base44 prototyping.

Do not create a backend/database.

The same service records should be reusable later by:

- Home featured services
- Service Detail
- Booking
- Admin service management

Exact code architecture will be revisited during the Codex/local architecture pass.

---

# 14. Asset Direction

Use imagery that represents the service or result meaningfully.

Avoid random generic beauty stock images that make different services difficult to distinguish.

Because final asset normalization is deferred to the Codex/local refinement phase, Base44 does not need repeated refinement cycles for non-blocking image inconsistencies.

However, broken/missing assets should be logged in the UI Refinement Backlog.

---

# 15. Locale Requirements

Preserve the approved locale baseline:

- natural Persian UI copy
- RTL-native layout
- Vazirmatn
- Persian display digits
- Toman
- 24-hour time where relevant
- Jalali dates where relevant
- mixed RTL/LTR handling
- English technical routes

Do not add a language switcher.

---

# 16. Design Direction

Preserve Warm Luxury while making the page practical for browsing.

The page should feel:

- elegant
- calm
- premium
- clear
- visual
- easy to scan

Prefer:

- strong hierarchy
- restrained service cards/items
- warm neutral surfaces
- subtle borders
- limited Muted Rose accents
- meaningful imagery
- generous but controlled whitespace

Avoid:

- e-commerce marketplace aesthetics
- excessive badges
- every item floating with strong shadow
- giant pill filters
- excessive pink/gold
- glassmorphism
- heavy gradients
- decorative animation
- generic SaaS styling

---

# 17. Responsive Behavior

## Mobile

- category browsing must remain discoverable and touch-friendly
- service items should stack naturally
- price/duration/action hierarchy must remain clear
- avoid cramped multi-column cards
- avoid uncontrolled horizontal scrolling
- primary booking actions must remain reachable

## Tablet

Use width deliberately and allow a suitable multi-column layout if readability remains strong.

## Desktop

Use a scanning-friendly grid/list composition with controlled content width.

Do not create excessively wide cards with long unreadable lines.

Do not simply stretch the mobile layout.

---

# 18. Accessibility

Preserve:

- logical heading hierarchy
- keyboard-accessible category controls
- visible focus states
- sufficient contrast
- useful image alt text
- touch-friendly targets
- clear selected filter state beyond color alone where possible
- readable Persian typography

---

# 19. UI Review / Debt Policy

After Base44 generation, review the page for UI quality but do not automatically spend another Base44 generation cycle on non-blocking polish.

Log issues in:

`projects/salon-booking/docs/ui/ui-refinement-backlog.md`

Review specifically for:

- asset consistency
- broken images
- service-card consistency
- spacing rhythm
- typography/contrast
- category control usability
- mobile overflow
- CTA hierarchy
- RTL correctness

Blocking structural/usability problems should still be corrected before moving on.

---

# 20. Explicitly Out of Scope

Do not implement:

- production backend
- database
- real availability
- booking state engine
- real pricing engine
- promotions/discounts
- ratings/reviews
- popularity ranking
- search infrastructure
- recommendation engine
- service comparison tool
- new routes
- admin service CRUD
- payment
- authentication

Do not fully implement `/services/:serviceId` during this pass; it remains a placeholder until its own Page Spec/Prompt.

---

# 21. Definition of Done

Services v0.1 is ready for prototype acceptance when:

- `/services` is implemented beyond placeholder state
- service categories are understandable
- approximately 8–12 deterministic services provide meaningful browsing
- service items expose useful price/duration context
- users can navigate to service detail placeholders
- users can enter booking
- the page does not duplicate Service Detail content
- pricing language does not overstate precision
- no fake ratings/discounts/popularity claims are introduced
- Persian/RTL foundation remains intact
- Warm Luxury remains consistent with Home
- mobile/tablet/desktop compositions are intentional
- no unrelated routes/features are invented
- non-blocking visual issues are captured for later Codex refinement

---
