# Base44 Page Implementation — Specialist Profile

**Prompt Version:** 0.1  
**Target Route:** `/specialists/:specialistId`  
**Scope:** Specialist Profile page only  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

Implement the Specialist Profile page of the existing Persian beauty salon booking application.

This is a **page implementation pass**, not a foundation redesign, architecture pass, or data-model refactor.

Use the existing application foundation, Public Layout, routes, Persian/RTL behavior, Vazirmatn typography, design tokens, shared components, responsive patterns, and Warm Luxury visual language already established by the current public pages.

Implement **only `/specialists/:specialistId`** in this pass.

After completing the page, STOP.

Do not fully implement Booking, Gallery, or any other placeholder route.

---

# 1. Page Goal

Help visitors understand:

1. این متخصص در چه حوزه‌ای فعالیت می‌کند؟
2. چه خدماتی را ارائه می‌دهد؟
3. سبک و نمونه‌کارهای او چگونه است؟
4. آیا برای نیاز من مناسب به نظر می‌رسد؟
5. چطور با همین متخصص وارد رزرو شوم؟

Primary CTA:

**رزرو با این متخصص** → `/book`

The page should feel like a focused professional beauty profile, not a social network profile, résumé, or provider marketplace listing.

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
- established spacing/radius/shadow system
- current button/card patterns
- Persian display digits where applicable
- Toman formatting where applicable
- English technical route paths
- current responsive behavior
- existing UI polish

Do not redesign global navigation, layouts, or the design system.

---

# 3. Required Page Structure

Use this hierarchy:

1. Public Header
2. Breadcrumb / Back-to-Specialists Context
3. Specialist Hero / Profile Summary
4. About / Professional Focus
5. Services Offered
6. Representative Work / Portfolio Preview
7. Booking Context
8. Final Booking CTA
9. Public Footer

Keep the page focused and concise.

Do not invent unrelated marketing sections.

---

# 4. Dynamic Specialist Context

The route is dynamic:

`/specialists/:specialistId`

The implementation should visibly support different specialist IDs/slugs rather than behaving as a single hard-coded profile.

Use deterministic Persian prototype content and stable IDs/slugs consistent with the Specialists listing where practical.

Do not create a backend/database.

Do not spend this pass restructuring or consolidating the entire mock-data architecture.

For an unknown specialist ID, use a simple safe prototype fallback rather than building a complex error system.

---

# 5. Breadcrumb

Provide lightweight navigation context such as:

`متخصصان / نام متخصص`

Allow users to return to `/specialists`.

Requirements:

- correct RTL ordering
- correct directional icon behavior
- keyboard accessible
- visually secondary to the profile content

Do not introduce a new navigation pattern.

---

# 6. Specialist Hero / Profile Summary

Immediately communicate the specialist identity.

Include:

- portrait
- Persian name
- concise professional title/focus
- short natural Persian descriptor
- key specialties/services
- primary booking CTA

Primary CTA:

**رزرو با این متخصص** → `/book`

Use a portrait-led editorial composition consistent with Warm Luxury.

Do NOT add fabricated:

- ratings
- review counts
- awards
- certificates
- years of experience
- follower counts
- popularity labels

---

# 7. About / Professional Focus

Provide a concise Persian profile describing the specialist's working focus and style.

Useful content may include:

- main specialization areas
- types of beauty services they focus on
- short description of their professional approach/style

Keep the content customer-relevant and natural.

Do not create a long résumé or biography.

Do not invent credentials, awards, certificates, employment history, or experience duration.

---

# 8. Services Offered

Show approximately **3–5 relevant services** associated with the current specialist.

Each service item may include:

- service name
- concise context
- approximate duration or price where already established and useful
- link to `/services/:serviceId`

Keep this section lightweight.

Do not recreate the complete Services catalog.

Do not invent new service categories simply to fill the profile.

---

# 9. Representative Work / Portfolio Preview

Show approximately **3–6 representative images** where appropriate.

Purpose:

- communicate visual style
- support trust
- make the profile feel useful before booking

Requirements:

- coherent aspect ratios/crops
- beauty-work imagery relevant to the specialist
- restrained gallery composition
- responsive behavior
- meaningful alt text

A subtle action toward `/gallery` is allowed if it fits the existing navigation model.

Do NOT fully implement Gallery.

Do NOT add:

- likes
- comments
- engagement metrics
- social-media handles
- client testimonials
- fabricated before/after claims

---

# 10. Trust Rules

Trust should come from:

- clear professional focus
- relevant services
- coherent portrait
- representative work
- consistent presentation

Do NOT fabricate social proof or credentials.

No ratings, reviews, testimonials, awards, certificates, follower counts, popularity rankings, or unsupported “best specialist” claims.

---

# 11. Booking Context

Clearly communicate that the booking action relates to the currently viewed specialist.

Primary action:

**رزرو با این متخصص** → `/book`

During this Base44 prototype pass, do not build real persistence, backend state, or a complex specialist-transfer mechanism solely for this action.

Structure the UI naturally so selected-specialist context can be formalized later during the local/Codex/backend phase.

Do not show real availability or schedules.

---

# 12. Final Booking CTA

End with one clear conversion section consistent with the other public pages.

Primary action:

**رزرو با این متخصص** → `/book`

Avoid several competing primary CTAs.

---

# 13. Asset Direction

Portrait and portfolio imagery are central to this page.

Prefer:

- consistent portrait framing
- coherent portfolio crops
- professional but natural beauty imagery
- predictable aspect ratios
- stable responsive behavior

Do not redesign the site's global asset system.

Do not spend repeated generation effort polishing non-blocking asset inconsistencies; final normalization can happen during local/Codex refinement.

---

# 14. Persian / RTL Requirements

Preserve:

- natural Persian copy
- RTL-native composition
- Vazirmatn
- Persian display digits where applicable
- Toman formatting where service prices appear
- correct directional icon behavior
- intentional mixed RTL/LTR handling
- English technical route paths

Do not implement RTL through right-alignment alone.

Do not add a language switcher.

---

# 15. Warm Luxury Direction

The page should feel:

- personal
- elegant
- professional
- calm
- visual
- premium
- conversion-focused

Prefer:

- portrait-led editorial composition
- strong information hierarchy
- controlled whitespace
- warm neutral surfaces
- restrained Muted Rose accents
- selective card usage
- subtle borders
- minimal shadows

Avoid:

- social-media profile aesthetics
- corporate résumé styling
- marketplace/provider-ranking aesthetics
- excessive badges
- heavy gradients
- glassmorphism
- fake-luxury decoration
- generic SaaS styling

---

# 16. Responsive Implementation

## Mobile

- portrait, name, focus, and booking CTA must remain immediately understandable
- service items must remain readable and touch-friendly
- portfolio preview must not create awkward overflow
- avoid tiny metadata
- preserve comfortable Persian reading width

## Tablet

Use width intentionally and preserve the relationship between portrait/profile information and supporting content.

## Desktop

Use an editorial composition rather than stretching the mobile layout.

Keep specialist identity visually dominant.

---

# 17. Accessibility

Preserve:

- logical heading hierarchy
- meaningful image alt text
- keyboard-accessible links/buttons
- visible focus states
- sufficient contrast
- adequate touch targets
- readable Persian typography
- semantic breadcrumb/navigation behavior where practical

---

# 18. Explicitly Out of Scope

Do NOT implement:

- `/book` beyond its existing placeholder
- `/gallery` beyond its existing placeholder
- backend/database
- real availability or schedules
- authentication changes
- reviews/ratings/testimonials
- awards/certifications/experience claims not already defined
- social-media functionality
- portfolio management
- recommendation engine
- personalization
- admin functionality
- architecture/data-model refactoring
- new routes
- dark mode
- full i18n platform

---

# 19. Definition of Done

Specialist Profile v0.1 is complete when:

- `/specialists/:specialistId` is implemented beyond placeholder state
- the page responds coherently to different specialist IDs/slugs
- specialist identity and professional focus are immediately clear
- approximately 3–5 relevant services are represented without recreating the full catalog
- representative work is shown in a restrained portfolio preview
- primary booking CTA clearly routes to `/book`
- no fabricated ratings, reviews, testimonials, awards, experience, or popularity claims are introduced
- Persian/RTL foundation remains intact
- Warm Luxury remains consistent with existing public pages
- existing shared UI patterns are preserved
- responsive behavior is intentional
- accessibility basics are preserved
- no unrelated pages/features are implemented

Then STOP.

Do not implement Gallery, Booking, or another page.
