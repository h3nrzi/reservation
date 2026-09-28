# Base44 Page Implementation — Services

**Prompt Version:** 0.1  
**Target Route:** `/services`  
**Scope:** Services listing page only  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

Implement the Services listing page of the existing Persian beauty salon booking application.

This is a **page implementation pass**, not a foundation redesign.

Use the existing approved Foundation v0.2, Public Layout, routes, RTL behavior, typography, design tokens, and visual language already established by the Home page.

Implement **only `/services`** in this pass.

After completing the Services page, STOP.

Do not fully implement `/services/:serviceId`, `/book`, or any other placeholder route.

---

# 1. Page Goal

The page should help users efficiently answer:

1. چه خدماتی ارائه می‌شود؟
2. کدام خدمت برای نیاز من مناسب‌تر است؟
3. چطور جزئیات آن را ببینم یا وارد رزرو شوم؟

Primary next steps:

- open service detail → `/services/:serviceId`
- begin booking → `/book`

The page is a discovery and decision surface, not a dense marketplace catalog.

---

# 2. Preserve Existing Product & Design Foundation

Preserve:

- Persian-first UI
- native RTL direction
- Vazirmatn
- Warm Luxury
- existing Public Header/Footer
- warm neutral palette
- restrained Muted Rose accent
- semantic design-token usage
- approved radius/shadow/spacing system
- Persian digits
- Toman formatting
- English technical route paths
- responsive behavior established by the foundation

The Services page must clearly belong to the same application as Home.

Do not create a new visual system or unrelated card style.

---

# 3. Required Page Structure

Use this hierarchy:

1. Public Header
2. Services Intro / compact page hero
3. Category Navigation / Filter
4. Services Listing
5. Booking Guidance / contextual CTA
6. Final Booking CTA
7. Public Footer

Small compositional adjustments are allowed where they improve hierarchy or responsive behavior.

Do not invent unrelated marketing sections.

---

# 4. Services Intro

Create a concise Persian introduction that explains users can explore salon services before choosing what to book.

Keep the actual services visible reasonably early on the page.

Do not create an oversized marketing hero that forces users to scroll significantly before reaching the catalog.

A restrained editorial visual is acceptable if it supports the design without distracting from service discovery.

---

# 5. Service Categories

Use these prototype categories:

- همه خدمات
- مو
- میکاپ
- ناخن
- ابرو و مژه
- مراقبت و زیبایی

Create a simple RTL-friendly category browsing/filter control.

Requirements:

- clear selected state
- touch-friendly
- keyboard-accessible
- mobile-friendly
- no difficult/uncontrolled horizontal overflow
- no excessive pill styling

Do not build complex faceted filtering.

Do not build production search infrastructure.

---

# 6. Deterministic Service Data

Create approximately **8–12 deterministic Persian service records** across the categories.

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

Prefer reusable mock data rather than duplicating arbitrary literals throughout components.

Conceptually, each record may contain:

- `id`
- `slug`
- `name`
- `category`
- `shortDescription`
- `duration`
- `priceFrom` or `priceRange`
- `image`

Keep technical field names/IDs in English while user-facing values remain Persian.

Do not create a backend or database.

Do not over-engineer a production domain model.

---

# 7. Services Listing

Each service item should expose only decision-useful summary information.

Recommended content:

- service name
- category
- short natural Persian description
- representative duration or duration range
- representative starting price or price range
- relevant image where useful
- action to view details
- optional booking action if hierarchy remains clear

Examples:

`از ۱٬۲۵۰٬۰۰۰ تومان`

`حدود ۹۰ دقیقه`

or

`۹۰ تا ۱۲۰ دقیقه`

Do not overload service items with:

- full descriptions
- detailed preparation instructions
- complete specialist lists
- detailed policies
- complex price breakdowns

Those belong deeper in the experience.

---

# 8. Service Item Interaction

Preferred hierarchy:

1. Understand service
2. Understand approximate price/duration
3. View details
4. Book when ready

Service detail action should route to the existing dynamic placeholder:

`/services/:serviceId`

Use stable IDs/slugs from deterministic mock data so links are coherent.

Booking actions should route to:

`/book`

If a user starts booking from a service item, structure the prototype so preserving selected-service context would be possible later, but do NOT build real persistence, backend state, or a booking engine during this pass.

Avoid ambiguous nested interactions.

---

# 9. Pricing Rules

Use Persian digits and Toman.

When exact pricing is not appropriate, use honest wording such as:

- `از ... تومان`
- a clear price range

Do not imply false pricing precision.

Do not introduce:

- discounts
- crossed-out prices
- limited-time promotions
- popularity labels
- best-seller badges

unless explicitly required later.

---

# 10. Duration Rules

Duration should help users estimate the appointment commitment.

Use concise Persian presentation such as:

- `حدود ۶۰ دقیقه`
- `۹۰ تا ۱۲۰ دقیقه`

Do not imply scheduling precision that the current prototype does not support.

---

# 11. Booking Guidance

After or near the listing, provide a concise explanation that the next booking stage allows the customer to choose a suitable specialist and appointment time.

Possible CTA:

**شروع رزرو** → `/book`

Do not repeat the full Home booking tutorial.

Do not implement the booking flow here.

---

# 12. Final Booking CTA

Provide a clear final conversion opportunity.

Primary action:

**رزرو نوبت** → `/book`

Reuse the visual language established on Home rather than inventing a new CTA pattern.

---

# 13. Asset Direction

Use service/result imagery that meaningfully helps distinguish services.

Avoid random generic beauty stock imagery when it makes different services look interchangeable.

Do not spend generation effort trying to perfect every image asset during this pass.

Non-blocking image inconsistencies will be logged for the later Codex/local refinement phase.

Broken or missing images should still be visible during review and logged as UI debt.

---

# 14. Persian / RTL Requirements

The page must remain Persian-first and RTL-native.

Requirements:

- natural Persian UI copy
- proper RTL composition
- Vazirmatn
- Persian display digits
- Toman prices
- correct directional icon behavior
- intentional mixed RTL/LTR handling where necessary
- English technical routes

Do not implement RTL by merely right-aligning an LTR layout.

Do not add a language switcher.

---

# 15. Warm Luxury Direction

The page should feel:

- elegant
- calm
- premium
- clear
- visual
- easy to scan

Prefer:

- strong hierarchy
- controlled whitespace
- restrained service surfaces/cards
- warm neutral backgrounds
- subtle borders
- limited Muted Rose accents
- meaningful imagery
- minimal shadows

Avoid:

- marketplace/e-commerce aesthetics
- excessive badges
- heavy floating cards
- giant pill filters
- excessive pink or gold
- glassmorphism
- gradient-heavy UI
- decorative animation
- generic SaaS styling

---

# 16. Responsive Implementation

## Mobile

- category navigation must remain discoverable and usable
- service items should stack naturally
- price/duration/action hierarchy should remain obvious
- avoid cramped multi-column cards
- avoid uncontrolled horizontal overflow
- maintain comfortable touch targets

## Tablet

Use available width intentionally. A suitable multi-column layout is acceptable when readability remains strong.

## Desktop

Use a scanning-friendly grid or list composition with controlled widths.

Do not create excessively wide cards with long text lines.

Do not simply stretch the mobile composition.

---

# 17. Accessibility

Maintain:

- logical headings
- keyboard-accessible category controls
- visible focus states
- sufficient contrast
- meaningful image alt text
- touch-friendly targets
- understandable selected-filter state
- readable Persian typography

Do not rely solely on color to communicate category selection where avoidable.

---

# 18. UI Debt Policy

This page will receive a UI quality review after generation.

Do NOT proactively redesign the page repeatedly for minor visual polish during this Base44 pass.

Non-blocking issues will be logged in:

`projects/salon-booking/docs/ui/ui-refinement-backlog.md`

Likely review areas include:

- asset consistency
- broken images
- service-card consistency
- spacing rhythm
- typography/contrast
- category-filter usability
- mobile overflow
- CTA hierarchy
- RTL correctness

The later Codex/local phase will prioritize global/component fixes before page-specific polish.

---

# 19. Explicitly Out of Scope

Do NOT implement:

- `/services/:serviceId` beyond its existing placeholder
- production backend
- database
- real availability
- booking engine
- real pricing engine
- authentication
- payments
- reviews/ratings
- promotions/discounts
- popularity ranking
- recommendation engine
- comparison tool
- complex search infrastructure
- admin service CRUD
- new routes
- dark mode
- full i18n platform

---

# 20. Definition of Done

Services v0.1 is complete when:

- `/services` is fully implemented beyond its placeholder state
- the existing global foundation remains intact
- service categories are clear and usable
- approximately 8–12 deterministic Persian services are represented
- service items expose useful price and duration context
- service detail actions route to the existing dynamic detail placeholder
- booking actions route to `/book`
- the page does not duplicate full Service Detail content
- pricing language avoids false precision
- no fake ratings, discounts, scarcity, or popularity claims are introduced
- Persian/RTL behavior remains correct
- Warm Luxury remains consistent with Home
- responsive behavior is intentional
- accessibility basics are preserved
- no unrelated routes/features are implemented

Then STOP.

Do not implement Service Detail or any other page.

Wait for review and the next prompt.
