# Salon Booking Platform — Service Detail Page Spec

**Version:** 0.1  
**Status:** Approved for Page Prompt Drafting  
**Route:** `/services/:serviceId`  
**Surface:** Customer / Public  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

## Purpose

Define the product, content hierarchy, interactions, and responsive intent for an individual service page before Base44 implementation.

The page should turn service discovery into a confident booking decision without becoming a long marketing landing page.

---

# 1. Primary Goal

Help a visitor who has selected a service answer:

1. این خدمت دقیقاً چیست و چه نتیجه‌ای دارد؟
2. حدوداً چقدر زمان و هزینه نیاز دارد؟
3. آیا نکته‌ای هست که قبل از رزرو باید بدانم؟
4. چه متخصصانی این خدمت را ارائه می‌دهند؟
5. چطور همین خدمت را رزرو کنم؟

Primary CTA:

**رزرو این خدمت** → `/book`

Secondary navigation should allow returning to `/services` and exploring relevant specialists where appropriate.

---

# 2. Page Role

This page primarily supports:

- **Understanding** — explain the selected service clearly.
- **Trust** — show useful service/result context without fabricated claims.
- **Decision** — provide price, duration, preparation, and specialist context.
- **Conversion** — move the visitor into booking with the service conceptually selected.

Do not duplicate the complete booking flow here.

---

# 3. Recommended Hierarchy

1. Public Header
2. Breadcrumb / Back-to-Services Context
3. Service Hero / Summary
4. Service Overview
5. What to Expect / Key Information
6. Suitable Specialists
7. Preparation / Important Notes
8. Related Services
9. Final Booking CTA
10. Public Footer

Keep the page concise enough that booking remains the obvious next step.

---

# 4. Breadcrumb / Navigation Context

Provide lightweight context such as:

`خدمات / رنگ و لایت`

The user should be able to return to `/services` easily.

RTL ordering and directional icons must be correct.

Do not introduce a new global navigation pattern.

---

# 5. Service Hero / Summary

The top section should immediately identify the selected service.

Recommended content:

- service name
- category
- concise one- or two-sentence description
- representative service/result image
- representative duration
- representative starting price or price range
- primary booking CTA

Example:

**رنگ و لایت**

`از ۱٬۲۵۰٬۰۰۰ تومان`

`حدود ۹۰ تا ۱۲۰ دقیقه`

Primary CTA:

**رزرو این خدمت** → `/book`

Avoid oversized decorative hero treatments that bury the useful service information.

---

# 6. Service Overview

Explain the service in natural Persian with enough detail to support a booking decision.

Cover only useful customer-facing context such as:

- what the service generally includes
- intended result / use case
- meaningful variation in the service where relevant

Do not make medical, guaranteed-result, or unsupported superiority claims.

Do not turn this into a long SEO article.

---

# 7. Key Information / What to Expect

Present the most decision-relevant facts in a compact, scan-friendly way.

Potential information:

- approximate duration
- starting price / price range
- whether final price may depend on factors such as hair length, complexity, or selected option
- general appointment expectations

Use honest prototype language rather than false precision.

Do not invent operational policies that have not been defined.

---

# 8. Pricing Communication

Use Persian digits and Toman.

Prefer:

- `از ... تومان`
- a representative price range

Where pricing may vary, explain the reason briefly rather than implying a fixed final amount.

Do not add discounts, fake promotions, crossed-out pricing, urgency/scarcity, or undefined packages.

---

# 9. Duration Communication

Use approximate customer-friendly duration such as:

- `حدود ۶۰ دقیقه`
- `۹۰ تا ۱۲۰ دقیقه`

Do not imply exact scheduling guarantees.

---

# 10. Suitable Specialists

Show a small number of representative specialists who can conceptually provide this service, approximately **2–3 people** where suitable.

Each preview may include:

- Persian name
- portrait
- specialty/focus
- short relevant descriptor
- link to specialist profile placeholder
- booking entry where useful

Provide a route toward `/specialists/:specialistId` where the existing route model supports it.

Do not fabricate ratings, review counts, awards, or popularity rankings.

This is not the full Specialists listing page.

---

# 11. Preparation / Important Notes

If the service benefits from preparation guidance, show a short practical section.

Keep it concise and clearly informational.

Do not invent strict cancellation, deposit, medical, or salon policies that have not been approved elsewhere.

If no meaningful preparation is needed for a service, omit the section rather than filling it with generic content.

---

# 12. Related Services

Show approximately **2–3 genuinely related services** to support continued discovery.

Examples:

- رنگ و لایت → بالیاژ / تراپی مو / براشینگ
- مانیکور → ژلیش / پدیکور

Each related item should remain lightweight and route back into the existing service detail pattern.

Do not create recommendation logic or personalization.

Avoid turning the bottom of the page into another full services catalog.

---

# 13. Booking Context

The booking CTA should conceptually carry the selected service into the future booking experience.

During Base44 prototyping, do not build backend persistence or a complex state engine solely for this.

It is sufficient that the UI clearly communicates **رزرو این خدمت** and routes toward `/book`.

The eventual local/Codex/backend phase can formalize how selected service context is transferred.

---

# 14. Final Booking CTA

End with a clear conversion section consistent with Home and Services.

Primary action:

**رزرو این خدمت** → `/book`

Avoid adding multiple competing primary CTAs.

---

# 15. Dummy Data Policy

Use deterministic Persian prototype content for the selected service.

The dynamic route should visibly support more than one service ID/slug rather than being hard-coded visually as a one-off static marketing page.

Reuse existing service concepts/content where practical during Base44 prototyping.

Do not create a backend/database.

Do not spend this page pass on architecture or data-model refactoring.

---

# 16. Asset Direction

Use imagery meaningfully related to the selected service/result.

Preserve the existing visual direction and assets where suitable.

Do not spend additional Base44 cycles perfecting non-blocking asset inconsistencies; log them for the local/Codex refinement phase.

Broken images or clearly incorrect service imagery should be captured in the UI backlog during review.

---

# 17. Locale Requirements

Preserve:

- Persian-first copy
- RTL-native composition
- Vazirmatn
- Persian display digits
- Toman prices
- 24-hour time where applicable
- Jalali date presentation where applicable
- correct mixed RTL/LTR handling
- English technical route paths

Do not add a language switcher.

---

# 18. Design Direction

Preserve Warm Luxury and the established Public UI.

The page should feel elegant, calm, informative, premium, visually confident, and conversion-focused.

Prefer editorial image/content composition, clear information hierarchy, controlled whitespace, warm neutral surfaces, restrained Muted Rose accents, subtle borders, and selective card usage.

Avoid marketplace/product-store aesthetics, excessive cards/badges, fake luxury decoration, heavy gradients, excessive shadows, glassmorphism, giant pills, and generic SaaS styling.

---

# 19. Responsive Behavior

## Mobile

- service name, price, duration, and booking CTA must remain immediately understandable
- hero composition should stack naturally
- specialist previews must remain touch-friendly
- related services should not create awkward overflow
- avoid overly small metadata
- preserve comfortable reading width

## Tablet

Use available width intentionally and preserve the relationship between service imagery and decision information.

## Desktop

Use editorial composition rather than simply stretching mobile sections.

Keep the primary service information visually dominant.

---

# 20. Accessibility

Preserve logical heading hierarchy, meaningful image alt text, keyboard-accessible links/buttons, visible focus states, sufficient contrast, adequate touch targets, readable Persian typography, and semantic navigation/breadcrumb behavior where practical.

---

# 21. UI Review / Debt Policy

After generation, review the page but defer non-blocking polish to the existing UI refinement backlog/local Codex phase.

Review specifically for hero balance, CTA prominence, information density, image consistency, specialist-card consistency, mobile typography, spacing rhythm, accent-text contrast, related-service layout, and RTL breadcrumb/directional behavior.

Blocking product/interaction issues should still be corrected before prototype acceptance.

---

# 22. Explicitly Out of Scope

Do not implement backend/database, real booking state persistence, real availability, payment, authentication changes, real pricing engine, reviews/ratings, promotions, recommendation engine, personalization, medical guidance, new product capabilities, admin functionality, or architecture refactoring.

Do not fully implement Specialist Detail or Booking during this pass.

---

# 23. Definition of Done

Service Detail v0.1 is ready for prototype acceptance when:

- `/services/:serviceId` is implemented beyond placeholder state
- selected service identity is immediately clear
- price and duration context are visible
- service explanation is useful but concise
- suitable specialist previews are represented where appropriate
- preparation/important notes are used only when meaningful
- related services support continued discovery without becoming another catalog
- booking CTA is clear and routes to `/book`
- no fake ratings/promotions/scarcity claims are introduced
- Persian/RTL foundation remains intact
- Warm Luxury remains consistent with Home and Services
- responsive behavior is intentional
- accessibility basics are preserved
- no unrelated pages/features are implemented
- non-blocking visual issues can be logged for later Codex refinement

---

# Next Step

Service Detail Page Spec v0.1  
→ Base44 Service Detail Prompt v0.1  
→ Generate `/services/:serviceId` Only  
→ Product/Structure Review  
→ UI Review & Debt Logging  
→ Accept Prototype  
→ Next Page Spec
