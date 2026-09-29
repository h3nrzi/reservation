# Base44 Page Implementation — Specialists

**Prompt Version:** 0.1  
**Target Route:** `/specialists`  
**Scope:** Specialists listing page only  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

Implement the Specialists listing page of the existing Persian beauty salon booking application.

This is a **page implementation pass**, not a foundation redesign, architecture pass, or data-model refactor.

Use the existing approved application foundation, Public Layout, routes, Persian/RTL behavior, Vazirmatn typography, design tokens, components, responsive patterns, and Warm Luxury visual language already established by Home, Services, and Service Detail.

Implement **only `/specialists`** in this pass.

After completing the Specialists page, STOP.

Do not fully implement Specialist Profile, Booking, Gallery, or any other placeholder route.

---

# 1. Page Goal

Help visitors answer:

1. چه متخصصانی در سالن فعالیت می‌کنند؟
2. هر متخصص بیشتر در چه خدماتی تخصص دارد؟
3. کدام متخصص با نیاز من مرتبط‌تر است؟
4. چطور پروفایل متخصص را ببینم یا وارد رزرو شوم؟

Primary next steps:

- view specialist profile → `/specialists/:specialistId`
- begin booking → `/book`

The page should feel like a curated introduction to the salon team, not a corporate employee directory or ranked marketplace.

---

# 2. Preserve Existing Foundation

Preserve:

- Persian-first UI
- native RTL direction
- Vazirmatn
- Warm Luxury
- existing Public Header/Footer
- warm neutral palette
- restrained Muted Rose accent
- semantic design tokens
- existing spacing/radius/shadow system
- established button/card patterns
- Persian display digits where applicable
- English technical route paths
- current responsive behavior
- existing UI polish from previous public pages

Do not redesign shared navigation, global layouts, or the design system.

---

# 3. Required Page Structure

Use this hierarchy:

1. Public Header
2. Specialists Intro / Compact Hero
3. Lightweight Specialty Filter if useful
4. Specialists Listing
5. Booking Guidance
6. Final Booking CTA
7. Public Footer

Keep the team listing reasonably high on the page.

Do not invent unrelated marketing sections.

---

# 4. Intro / Compact Hero

Create a concise natural Persian introduction explaining that customers can get to know the salon specialists and choose a suitable person based on the service they need.

Keep it restrained and editorial.

Do not create an oversized decorative hero that pushes the specialists far below the fold.

---

# 5. Deterministic Specialist Data

Create approximately **6–8 deterministic Persian specialist records**.

Use stable IDs/slugs so each specialist can link coherently to:

`/specialists/:specialistId`

Conceptually each record may contain:

- `id`
- `slug`
- `name`
- `portrait`
- `title` or professional focus
- `specialties`
- `shortBio`
- relevant service IDs/slugs

Keep technical field names/IDs in English and user-facing content in Persian.

Do not create a backend/database.

Do not spend this pass consolidating or restructuring the entire mock-data architecture.

---

# 6. Specialist Content

Each specialist preview should prioritize decision-useful information:

- Persian name
- portrait
- concise professional focus/title
- approximately 2–4 relevant specialties/services
- short natural Persian descriptor
- profile action
- optional booking action if hierarchy remains clean

Representative professional focuses may include:

- متخصص رنگ و لایت
- میکاپ آرتیست
- متخصص ناخن
- متخصص ابرو و مژه
- استایلیست مو
- متخصص مراقبت و تراپی مو

Use professional, natural wording.

Do not use exaggerated titles or unsupported claims.

---

# 7. Trust Rules

Do NOT fabricate:

- ratings
- review counts
- awards
- certificates
- years of experience
- follower counts
- popularity rankings
- “بهترین متخصص” labels
- artificial scarcity

Trust should come from clear professional focus, coherent portraits, service context, and the ability to explore individual profiles later.

---

# 8. Specialty Filtering

If useful for the 6–8 person dataset, provide a lightweight RTL-friendly filter using the established service taxonomy:

- همه متخصصان
- مو
- میکاپ
- ناخن
- ابرو و مژه
- مراقبت و زیبایی

Requirements:

- clear selected state
- touch-friendly
- keyboard-accessible
- usable on mobile
- no uncontrolled horizontal overflow
- no excessive pill styling

Do not build complex faceted filtering or production search infrastructure.

If the page is clearer without filtering, a straightforward specialist listing is acceptable.

---

# 9. Specialist Card / Preview Interaction

Preferred hierarchy:

1. Recognize specialist
2. Understand professional focus
3. Understand relevant specialties/services
4. View profile
5. Book when ready

Profile action:

`/specialists/:specialistId`

Booking action:

`/book`

Do not fully implement either destination during this pass.

Avoid ambiguous nested click targets if multiple actions exist.

Do not overload cards with full bios, portfolios, schedules, availability, or operational information.

---

# 10. Portrait Direction

Portrait consistency is important on this page.

Prefer:

- consistent aspect ratio
- similar framing/crop
- coherent visual quality and lighting
- professional but natural beauty-salon portraits
- predictable image behavior across breakpoints

Keep the existing asset approach where practical.

Do not spend repeated generation effort perfecting non-blocking imagery.

Do not redesign the global asset system.

---

# 11. Booking Guidance

Include concise Persian guidance explaining that the customer may choose a specialist by exploring profiles or continue into booking and make the choice as part of the reservation flow.

Possible CTA:

**شروع رزرو** → `/book`

Keep this section compact.

Do not reproduce the complete booking tutorial.

---

# 12. Final Booking CTA

End with a clear conversion opportunity consistent with the existing public pages.

Primary action:

**رزرو نوبت** → `/book`

Maintain the existing CTA hierarchy and avoid several competing primary actions.

---

# 13. Persian / RTL Requirements

Preserve:

- natural Persian copy
- RTL-native composition
- Vazirmatn
- Persian display digits where applicable
- correct directional icon behavior
- intentional mixed RTL/LTR handling
- English technical route paths

Do not implement RTL through right-alignment alone.

Do not add a language switcher.

---

# 14. Warm Luxury Direction

The page should feel:

- elegant
- human
- calm
- professional
- premium
- easy to scan

Prefer:

- portrait-led composition
- strong typography hierarchy
- controlled whitespace
- warm neutral surfaces
- restrained Muted Rose accents
- subtle borders
- selective/minimal shadows

Avoid:

- corporate staff-directory styling
- marketplace/provider-ranking aesthetics
- excessive badges
- heavy floating cards
- fake luxury decoration
- excessive pink/gold
- heavy gradients
- glassmorphism
- giant pills
- generic SaaS styling

---

# 15. Responsive Implementation

## Mobile

- portraits and names must remain prominent
- professional focus and specialties must remain readable
- actions must be touch-friendly
- avoid tiny metadata
- avoid uncontrolled horizontal overflow
- specialist items should stack naturally
- category controls, if present, must remain discoverable

## Tablet

Use available width deliberately and use a suitable multi-column composition when readability remains strong.

## Desktop

Use a balanced team grid/list with controlled content width and consistent portrait treatment.

Avoid accidental orphan-card imbalance where practical through layout behavior, without changing the required dataset merely to make the grid look full.

Do not simply stretch the mobile composition.

---

# 16. Accessibility

Preserve:

- logical heading hierarchy
- meaningful portrait alt text
- keyboard-accessible links/buttons/filter controls
- visible focus states
- sufficient contrast
- adequate touch targets
- readable Persian typography
- selected filter state beyond color alone where practical

---

# 17. Explicitly Out of Scope

Do NOT implement:

- `/specialists/:specialistId` beyond its existing placeholder
- `/book` beyond its existing placeholder
- Gallery
- backend/database
- real availability
- schedules
- authentication changes
- reviews/ratings
- popularity ranking
- awards/certifications not already defined
- recommendation engine
- personalization
- admin functionality
- architecture/data-model refactoring
- new routes
- dark mode
- full i18n platform

---

# 18. Definition of Done

Specialists v0.1 is complete when:

- `/specialists` is implemented beyond placeholder state
- approximately 6–8 deterministic Persian specialists are represented
- each specialist's professional focus is understandable at a glance
- relevant specialties/services are visible without overloading the listing
- profile actions route to `/specialists/:specialistId`
- booking entry routes to `/book`
- no fabricated ratings, reviews, awards, experience claims, or popularity labels are introduced
- portrait treatment is reasonably coherent
- Persian/RTL foundation remains intact
- Warm Luxury remains consistent with existing public pages
- existing shared UI patterns are preserved
- responsive behavior is intentional
- accessibility basics are preserved
- no unrelated pages/features are implemented

Then STOP.

Do not implement Specialist Profile or another page.
