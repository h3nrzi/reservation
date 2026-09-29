# Salon Booking Platform — Specialists Page Spec

**Version:** 0.1  
**Status:** Approved for Page Prompt Drafting  
**Route:** `/specialists`  
**Surface:** Customer / Public  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

## Purpose

Define the public Specialists listing page before Base44 implementation.

This page should help visitors discover the salon team, understand each specialist's focus, and move naturally toward a specialist profile or booking.

---

# 1. Primary Goal

Help visitors answer:

1. چه متخصصانی در سالن فعالیت می‌کنند؟
2. هر متخصص بیشتر در چه خدماتی تخصص دارد؟
3. کدام متخصص با نیاز من مرتبط‌تر است؟
4. چطور پروفایل متخصص را ببینم یا وارد رزرو شوم؟

Primary next steps:

- View specialist profile → `/specialists/:specialistId`
- Begin booking → `/book`

---

# 2. Page Role

The page supports:

- **Discovery** — introduce the salon team.
- **Differentiation** — make specialist focus areas understandable.
- **Trust** — provide useful professional context without fabricated social proof.
- **Decision** — open an individual specialist profile.
- **Conversion** — enter booking when the visitor is ready.

This is not a staff-management page and should not expose internal operational information.

---

# 3. Recommended Structure

1. Public Header
2. Specialists Intro / Compact Hero
3. Optional Specialty/Service Filter
4. Specialists Listing
5. Booking Guidance
6. Final Booking CTA
7. Public Footer

Keep the specialists visible reasonably early on the page.

---

# 4. Intro / Compact Hero

Use a concise Persian introduction explaining that customers can become familiar with the salon specialists and choose a suitable person based on the service they need.

Avoid a large decorative hero that pushes the team listing far below the fold.

A restrained editorial image or composition is acceptable if it supports the existing Warm Luxury direction.

---

# 5. Specialist Dataset

Use approximately **6–8 deterministic Persian specialist records** so the page feels realistic enough for discovery and responsive layout testing.

Each specialist may conceptually contain:

- `id`
- `slug`
- `name`
- `portrait`
- `title` or professional focus
- `specialties`
- short bio/descriptor
- relevant service IDs/slugs

Use stable IDs/slugs so profiles can route consistently to `/specialists/:specialistId`.

Do not create a backend/database.

Do not spend this page pass restructuring the entire mock-data architecture.

---

# 6. Specialist Information

Each specialist preview should prioritize information useful for choosing who to explore further.

Recommended content:

- Persian name
- portrait
- concise professional title/focus
- 2–4 relevant specialties/services
- short natural Persian descriptor
- action to view profile
- optional booking action if the hierarchy remains clear

Example focus labels might include concepts such as:

- متخصص رنگ و لایت
- میکاپ آرتیست
- متخصص ناخن
- متخصص ابرو و مژه
- استایلیست مو

Use natural wording rather than inflated marketing titles.

---

# 7. Trust & Social Proof Rules

Do NOT fabricate:

- star ratings
- review counts
- awards
- certificates
- years of experience
- follower counts
- popularity rankings
- “بهترین متخصص” labels

unless such data has explicitly been defined elsewhere.

Trust should come from clear presentation, professional focus, imagery, service context, and later portfolio/profile content.

---

# 8. Filtering / Browsing

A lightweight specialty/service filter may be used if it genuinely improves browsing.

Possible options can correspond to the established service taxonomy, for example:

- همه متخصصان
- مو
- میکاپ
- ناخن
- ابرو و مژه
- مراقبت و زیبایی

Requirements:

- simple selected state
- RTL-friendly
- keyboard accessible
- mobile usable
- no complex faceted filtering
- no production search infrastructure

If the page remains clearer without filtering at the current dataset size, a straightforward listing is acceptable.

---

# 9. Specialist Card / Preview Behavior

Preferred information hierarchy:

1. Recognize the specialist
2. Understand their professional focus
3. Understand relevant services/specialties
4. View profile
5. Book when ready

Primary profile route:

`/specialists/:specialistId`

Booking route:

`/book`

Avoid ambiguous nested interactions if both profile and booking actions exist on the same card.

Do not overload cards with full bios, portfolio galleries, schedules, or availability.

---

# 10. Portrait / Asset Direction

Portraits are especially important on this page.

Prefer:

- consistent portrait aspect ratio
- similar crop/framing
- coherent lighting/quality
- professional but natural beauty-salon imagery
- graceful visual fallback behavior

Avoid a mixture of unrelated photography styles that makes the team feel visually disconnected.

Do not spend repeated Base44 cycles perfecting non-blocking asset inconsistencies; final normalization can happen during the Codex/local refinement phase.

---

# 11. Booking Guidance

Provide a concise explanation that users can choose a specialist now or continue to booking and make their specialist preference during the booking flow.

Possible CTA:

**شروع رزرو** → `/book`

Do not implement the booking flow on this page.

---

# 12. Final Booking CTA

Provide one clear conversion opportunity consistent with Home, Services, and Service Detail.

Primary action:

**رزرو نوبت** → `/book`

Keep the CTA hierarchy restrained and avoid multiple competing primary actions.

---

# 13. Locale Requirements

Preserve the established locale baseline:

- natural Persian copy
- RTL-native composition
- Vazirmatn
- Persian display digits where applicable
- correct directional icons
- intentional mixed RTL/LTR handling
- English technical route paths

Do not add a language switcher.

---

# 14. Design Direction

Preserve Warm Luxury and the existing Public UI.

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

- corporate employee-directory aesthetics
- marketplace/provider-ranking aesthetics
- excessive badges
- heavy floating cards
- fake luxury decoration
- heavy gradients
- glassmorphism
- excessive pills
- generic SaaS styling

---

# 15. Responsive Behavior

## Mobile

- portraits and names must remain visually clear
- professional focus/specialties must remain readable
- actions must be touch-friendly
- avoid overly dense metadata
- avoid uncontrolled horizontal overflow
- cards/items should stack naturally

## Tablet

Use width deliberately and allow a suitable multi-column composition when readability remains strong.

## Desktop

Use a balanced team grid/list composition with controlled widths and consistent portrait treatment.

Avoid awkward orphan cards where practical.

Do not simply stretch the mobile layout.

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
- selected filter state that does not rely only on color where practical

---

# 17. Explicitly Out of Scope

Do not implement:

- Specialist Profile beyond its existing placeholder
- Booking beyond its existing placeholder
- backend/database
- real specialist availability
- schedules
- authentication
- reviews/ratings
- popularity ranking
- awards/certifications not already defined
- recommendation engine
- personalization
- admin functionality
- architecture/data-model refactoring
- new routes

---

# 18. Definition of Done

Specialists v0.1 is complete when:

- `/specialists` is implemented beyond placeholder state
- approximately 6–8 deterministic Persian specialists are represented
- specialist professional focus is understandable at a glance
- relevant specialties/services are visible without overloading cards
- profile actions route to `/specialists/:specialistId`
- booking entry routes to `/book`
- no fabricated ratings/reviews/awards/popularity claims are introduced
- portrait treatment is reasonably coherent
- Persian/RTL foundation remains intact
- Warm Luxury remains consistent with existing public pages
- responsive behavior is intentional
- accessibility basics are preserved
- no unrelated pages/features are implemented

---

# Next Step

Specialists Page Spec v0.1  
→ Base44 Specialists Prompt v0.1  
→ Generate `/specialists` Only  
→ Next Page: Specialist Profile
