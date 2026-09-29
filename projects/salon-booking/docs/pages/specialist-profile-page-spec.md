# Salon Booking Platform — Specialist Profile Page Spec

**Version:** 0.1  
**Status:** Approved for Page Prompt Drafting  
**Route:** `/specialists/:specialistId`  
**Surface:** Customer / Public  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

## Purpose

Define the public Specialist Profile page before Base44 implementation.

The page should help a visitor understand an individual specialist's professional focus, relevant services and representative work, then move naturally toward booking.

---

# 1. Primary Goal

Help visitors answer:

1. این متخصص در چه حوزه‌ای فعالیت می‌کند؟
2. چه خدماتی را ارائه می‌دهد؟
3. سبک و نمونه‌کارهای او چگونه است؟
4. آیا برای نیاز من مناسب به نظر می‌رسد؟
5. چطور با این متخصص وارد رزرو شوم؟

Primary CTA:

**رزرو با این متخصص** → `/book`

Secondary actions may lead to relevant service details or the specialists listing.

---

# 2. Page Role

The page supports:

- **Understanding** — communicate the specialist's professional focus.
- **Trust** — provide useful profile and representative work context without fabricated social proof.
- **Service Discovery** — expose relevant services offered by the specialist.
- **Decision** — help the visitor decide whether to continue with this specialist.
- **Conversion** — enter booking with the specialist conceptually selected.

This is not a social-media profile, résumé, or staff-management page.

---

# 3. Recommended Structure

1. Public Header
2. Breadcrumb / Back-to-Specialists Context
3. Specialist Hero / Profile Summary
4. About / Professional Focus
5. Services Offered
6. Representative Work / Portfolio Preview
7. Booking Context
8. Final Booking CTA
9. Public Footer

Keep the page focused and avoid unnecessary biography or marketing sections.

---

# 4. Dynamic Specialist Context

The route is dynamic:

`/specialists/:specialistId`

The page should visibly support different specialist IDs/slugs rather than behaving as one hard-coded profile.

Use deterministic Persian prototype content and stable IDs/slugs.

Do not create a backend/database.

Do not spend this pass restructuring the entire mock-data architecture.

For an unknown ID, use a simple safe prototype fallback rather than building a complex error system.

---

# 5. Breadcrumb / Navigation Context

Provide lightweight context such as:

`متخصصان / نام متخصص`

Allow an easy return to `/specialists`.

Requirements:

- correct RTL order
- correct directional icon behavior
- keyboard accessible
- visually secondary to the profile itself

---

# 6. Specialist Hero / Profile Summary

Immediately communicate who the specialist is and what they focus on.

Recommended content:

- portrait
- Persian name
- concise professional title/focus
- short natural descriptor
- key specialties/services
- primary booking CTA

Primary CTA:

**رزرو با این متخصص** → `/book`

Use an editorial, portrait-led composition consistent with Warm Luxury.

Do not introduce fabricated ratings, review counts, awards, follower counts, experience years, or popularity labels.

---

# 7. About / Professional Focus

Provide a concise Persian profile explaining the specialist's working focus and style.

Useful content may include:

- main areas of specialization
- type of beauty work they focus on
- short description of their approach/style

Keep this professional and customer-relevant.

Do not invent credentials, certificates, awards, employment history, or years of experience unless explicitly defined by the product later.

Do not create a long résumé or biography.

---

# 8. Services Offered

Show approximately **3–5 relevant services** associated with the specialist.

Each item should remain lightweight and may include:

- service name
- short context
- approximate duration/price context where already established and useful
- link to `/services/:serviceId`

Do not recreate the complete Services catalog.

Do not introduce new service categories merely to fill the profile.

---

# 9. Representative Work / Portfolio Preview

Show a compact visual preview of representative work, approximately **3–6 images** where appropriate.

The purpose is to help users understand the specialist's visual style and build confidence before booking.

Requirements:

- coherent image aspect ratios/crops
- visually relevant beauty-work imagery
- restrained gallery composition
- useful alt text
- responsive behavior

Do not fabricate likes, comments, engagement metrics, social-media handles, before/after claims, or client testimonials.

Do not build a full portfolio management system.

If the existing product has a Gallery route, the section may include a subtle action toward `/gallery`, but do not implement Gallery during this pass.

---

# 10. Trust Rules

Trust should come from:

- clear professional focus
- relevant services
- coherent portrait
- representative work
- consistent product presentation

Do NOT fabricate:

- ratings
- review counts
- testimonials
- awards
- certificates
- years of experience
- follower counts
- popularity ranking
- "best specialist" claims

---

# 11. Booking Context

The page should clearly communicate that the user is booking with the currently viewed specialist.

Primary action:

**رزرو با این متخصص** → `/book`

During Base44 prototyping, do not build real persistence or backend booking state solely to transfer the selected specialist.

Structure the UI so that selected-specialist context can be formalized later during local/Codex/backend implementation.

Do not expose real availability or schedules here.

---

# 12. Final Booking CTA

End with one clear conversion section consistent with the other public pages.

Primary action:

**رزرو با این متخصص** → `/book`

Avoid multiple competing primary CTAs.

---

# 13. Asset Direction

Portrait and portfolio imagery are central to this page.

Prefer:

- consistent portrait framing
- coherent portfolio crops
- professional but natural imagery
- predictable aspect ratios
- graceful image behavior across breakpoints

Do not spend repeated Base44 cycles perfecting non-blocking asset inconsistencies; final normalization can happen during the Codex/local refinement phase.

---

# 14. Locale Requirements

Preserve:

- natural Persian copy
- RTL-native composition
- Vazirmatn
- Persian display digits where applicable
- Toman formatting where service prices appear
- correct directional icons
- intentional mixed RTL/LTR handling
- English technical route paths

Do not add a language switcher.

---

# 15. Design Direction

Preserve Warm Luxury and the established Public UI.

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
- strong hierarchy
- controlled whitespace
- warm neutral surfaces
- restrained Muted Rose accents
- selective cards
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

# 16. Responsive Behavior

## Mobile

- portrait, name, focus, and booking CTA must remain immediately understandable
- service items should remain readable and touch-friendly
- portfolio preview must avoid awkward overflow
- avoid tiny metadata
- preserve comfortable Persian reading width

## Tablet

Use available width intentionally and preserve a clear relationship between portrait/profile information and supporting content.

## Desktop

Use an editorial composition rather than simply stretching the mobile layout.

Keep the specialist identity visually dominant.

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

Do not implement:

- Booking beyond its existing placeholder
- Gallery beyond its existing placeholder
- backend/database
- real availability/schedules
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

---

# 19. Definition of Done

Specialist Profile v0.1 is complete when:

- `/specialists/:specialistId` is implemented beyond placeholder state
- the page responds coherently to different specialist IDs/slugs
- specialist identity and professional focus are immediately clear
- relevant services are represented without recreating the full catalog
- representative work is shown in a restrained portfolio preview
- booking CTA clearly routes to `/book`
- no fabricated ratings/reviews/awards/experience/popularity claims are introduced
- Persian/RTL foundation remains intact
- Warm Luxury remains consistent with existing public pages
- responsive behavior is intentional
- accessibility basics are preserved
- no unrelated pages/features are implemented

---

# Next Step

Specialist Profile Page Spec v0.1  
→ Base44 Specialist Profile Prompt v0.1  
→ Generate `/specialists/:specialistId` Only  
→ Next Page: Gallery
