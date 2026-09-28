# Salon Booking Platform — Home Page Spec

**Version:** 0.1  
**Status:** Approved for Page Prompt Drafting  
**Route:** `/`  
**Surface:** Customer / Public  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

## Purpose

Define the product, content, hierarchy, interaction, and responsive intent for the Home page before asking Base44 to implement it.

This document describes what the page should accomplish. It should reduce the number of product/design decisions Base44 must invent during generation.

---

# 1. Primary Goal

Within the first few seconds, a visitor should understand:

- this is a premium women's beauty salon
- what kinds of services are available
- that specialist selection and online appointment booking are available
- that the salon's work can be evaluated visually
- how to begin booking

The primary conversion goal is to move qualified visitors into the booking flow.

Primary CTA:

**رزرو نوبت** → `/book`

Secondary CTA:

**مشاهده خدمات** → `/services`

---

# 2. Page Roles

Every major Home section should primarily support at least one of:

1. **Discovery** — help visitors understand services, specialists, or salon offering.
2. **Trust** — provide evidence that the salon and its specialists are credible and desirable.
3. **Conversion** — move visitors toward booking or a deeper product page.

Avoid adding sections solely because they are common on marketing websites.

Home should not become an excessively long landing page that duplicates dedicated pages.

---

# 3. Approved Section Hierarchy

1. Header / Public Navigation
2. Hero
3. Featured Services
4. Why Ara
5. Featured Specialists
6. Portfolio / Gallery Preview
7. How Booking Works
8. Trust / Social Proof
9. FAQ Preview
10. Final Booking CTA
11. Footer

This is the initial hierarchy. Base44 may make small compositional decisions inside sections but should not invent major new Home sections without explicit need.

---

# 4. Header

Use the existing Public Layout foundation rather than creating a new page-specific navigation system.

Representative Persian navigation should provide access to key public destinations such as:

- خانه
- خدمات
- متخصصان
- گالری
- سوالات متداول

Primary header action:

**رزرو نوبت**

The header should be RTL-native and responsive.

Avoid overcrowding the navigation.

---

# 5. Hero

## Purpose

Communicate salon positioning and immediately expose the booking action.

## Content Direction

Use concise natural Persian copy rather than generic translated marketing language.

The hero should communicate a premium, professional beauty experience and convenient online booking.

Do not use exaggerated claims such as "بهترین سالن ایران" or unverifiable superiority statements.

## Actions

Primary:

**رزرو نوبت** → `/book`

Secondary:

**مشاهده خدمات** → `/services`

## Visual Direction

Photography should have a meaningful role.

Prefer authentic-looking premium salon / beauty-result imagery rather than abstract SaaS illustrations.

The composition should feel editorial and spacious while preserving clear CTA hierarchy.

Avoid text-over-image treatments that damage Persian readability or contrast.

---

# 6. Featured Services

## Purpose

Help visitors quickly understand the salon offering and enter service discovery.

Show approximately **4–6 representative services** using deterministic Persian dummy data.

Potential examples may include:

- رنگ و لایت
- کوتاهی و استایل مو
- میکاپ
- خدمات ناخن
- ابرو و مژه
- مراقبت و زیبایی مو

Exact service taxonomy remains prototype data and may evolve later.

Each service preview may contain only useful summary information such as:

- service name
- short description
- representative duration
- representative starting price
- relevant image where useful

Use Persian digits and Toman formatting.

Provide a clear route to `/services` and/or relevant service detail pages.

Do not turn Home into the complete service catalog.

---

# 7. Why Ara

## Purpose

Explain the salon's value proposition without generic icon-grid marketing filler.

Focus on a small number of meaningful differentiators, for example:

- انتخاب متخصص متناسب با خدمت
- مشاهده زمان‌های قابل رزرو
- رزرو آنلاین ساده و شفاف
- تمرکز بر کیفیت و تجربه حرفه‌ای

Keep this section concise.

Avoid unsupported quantitative claims.

Avoid creating six generic cards simply to fill space.

---

# 8. Featured Specialists

## Purpose

Build trust and show that customers can choose who provides the service.

Show approximately **3 representative specialists**.

Each preview may include:

- Persian name
- specialty / focus
- portrait
- short useful descriptor
- link to specialist profile
- booking entry where appropriate

Use natural Persian dummy names and content.

Do not show fake ratings/review counts unless review functionality is explicitly introduced later.

Provide access to `/specialists`.

---

# 9. Portfolio / Gallery Preview

## Purpose

Provide visual evidence of work quality and encourage deeper gallery exploration.

Use a restrained image-led composition showing representative beauty work.

This section should feel more visual than card-heavy.

Provide access to `/gallery`.

Do not reproduce the entire Gallery page on Home.

Avoid decorative imagery unrelated to actual salon work.

---

# 10. How Booking Works

## Purpose

Reduce uncertainty about online booking.

Explain the process in approximately **3 simple stages**, rather than reproducing all six internal booking steps.

Suggested conceptual grouping:

1. خدمت و متخصص را انتخاب کنید
2. زمان مناسب را پیدا کنید
3. اطلاعات را تأیید و نوبت را ثبت کنید

The visual progression must make sense in RTL.

Keep copy concise and task-oriented.

Primary or secondary CTA may lead to `/book`.

---

# 11. Trust / Social Proof

## Purpose

Increase confidence without fabricating evidence.

Because real customer reviews and production metrics do not yet exist, do NOT invent:

- fake review counts
- fake star ratings
- fake customer numbers
- fake awards
- fake press logos
- fabricated testimonials presented as real

For the prototype, trust may instead come from truthful structural signals such as:

- professional specialist presentation
- clear service information
- portfolio imagery
- transparent booking flow
- salon environment / quality principles

If a testimonial-style visual placeholder is useful for future design exploration, it must be clearly understood as prototype content and not framed as verified real-world evidence.

---

# 12. FAQ Preview

## Purpose

Answer a small number of high-friction questions before booking.

Show approximately **3–4 representative questions**, such as:

- چطور نوبت رزرو کنم؟
- آیا می‌توانم متخصص موردنظرم را انتخاب کنم؟
- اگر نیاز به تغییر یا لغو نوبت داشته باشم چه کار کنم؟
- چه زمانی باید در سالن حاضر شوم؟

Keep answers concise on Home.

Provide access to `/faq` for the complete FAQ experience.

---

# 13. Final Booking CTA

## Purpose

Provide a clear conversion opportunity after the visitor has seen services, specialists, portfolio, and booking explanation.

Primary action:

**رزرو نوبت** → `/book`

The section should be visually distinct through composition and spacing rather than excessive gradients, shadows, or decoration.

---

# 14. Footer

Use the Public Layout footer foundation.

It may provide concise access to:

- public navigation
- salon/contact information placeholders
- About/Contact content where appropriate
- booking CTA

Do not create new About or Contact routes.

Keep placeholder contact information clearly prototype-oriented until real business details exist.

---

# 15. Dummy Data Policy

Home implementation should introduce a small deterministic Persian dummy-data set sufficient for the page.

Dummy data should be reusable later rather than repeated as arbitrary literals across components.

Use natural Persian examples for:

- services
- specialists
- prices
- durations
- FAQ

Do not build a backend or database.

Do not create an unnecessarily large data model during Home implementation.

---

# 16. Locale Requirements

The page must follow the approved locale baseline:

- Persian user-facing copy
- RTL-native layout
- Vazirmatn typography
- Persian digits for normal display
- Toman for prices
- 24-hour time where time appears
- Jalali/Persian date presentation where dates appear
- intentional mixed RTL/LTR handling
- English technical route paths

Do not add a language switcher.

---

# 17. Design Direction

Preserve the approved Warm Luxury direction.

Customer Home should feel:

- elegant
- warm
- calm
- premium
- modern
- visual
- spacious

Use:

- generous whitespace
- strong Persian typographic hierarchy
- restrained Muted Rose accent
- warm neutral surfaces
- subtle borders
- minimal shadows
- selective cards
- image-led composition where appropriate

Avoid:

- excessive pink
- excessive gold
- glassmorphism
- heavy gradients
- excessive shadows
- card-everything layout
- pill-everything styling
- generic SaaS appearance
- fake luxury styling
- decorative animation

---

# 18. Responsive Behavior

## Mobile

The page should remain conversion-focused and easy to scan.

- Hero CTA should remain obvious.
- Navigation should collapse appropriately.
- Image compositions should adapt without awkward cropping.
- Service/specialist previews should remain touch-friendly.
- Section spacing may reduce from desktop values while preserving hierarchy.
- Persian text should not be squeezed into narrow fixed-width components.

## Tablet

Use available width deliberately rather than simply scaling mobile.

## Desktop

Use editorial composition and whitespace.

Do not render the page as a stretched single-column mobile layout.

Respect the approved `content-max` while allowing intentional full-width visual sections where useful.

---

# 19. Interaction Guidance

Interactions should be subtle and purposeful.

Appropriate examples:

- clear hover/focus states
- image/card link feedback
- button feedback
- restrained section/image transitions if Base44 adds motion

Do not add decorative animation simply to make the page feel dynamic.

All interactive elements must have visible focus behavior.

---

# 20. Accessibility

Preserve:

- readable Persian typography
- sufficient contrast
- meaningful heading hierarchy
- useful alt text for meaningful images
- keyboard-accessible links/buttons
- visible focus states
- adequate touch targets
- non-color-only communication

Do not sacrifice contrast for a muted luxury aesthetic.

---

# 21. Explicitly Out of Scope for Home v0.1

Do not implement:

- production backend
- real booking logic
- authentication
- real reviews
- rating system
- payment
- notification delivery
- dynamic availability
- recommendation engine
- loyalty
- promotions
- memberships
- waitlist
- analytics dashboard
- new routes

Do not redesign the approved global foundation unless a Home requirement exposes a genuine foundation defect.

---

# 22. Home Definition of Done

Home v0.1 is ready for review when:

- `/` is fully designed beyond its previous placeholder state
- the approved section hierarchy is represented
- the primary booking CTA is clear
- service discovery is represented without duplicating `/services`
- specialist discovery is represented without duplicating `/specialists`
- gallery preview is image-led and links deeper
- booking explanation is concise and RTL-aware
- trust is established without fabricated claims
- FAQ preview remains concise
- final booking CTA exists
- page is Persian-first and RTL-native
- Warm Luxury direction is preserved
- dummy data is natural Persian and deterministic
- representative prices use Persian digits and Toman
- mobile/tablet/desktop layouts are intentional
- accessibility basics are preserved
- no unrelated product features/routes were invented

---
