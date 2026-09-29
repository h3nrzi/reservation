# Base44 Page Implementation — Service Detail

**Prompt Version:** 0.1  
**Target Route:** `/services/:serviceId`  
**Scope:** Service Detail page only  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

Implement the Service Detail page of the existing Persian beauty salon booking application.

This is a **page implementation pass**, not a foundation redesign, architecture pass, or data-model refactor.

Use the existing approved application foundation, Public Layout, routes, Persian/RTL behavior, typography, design tokens, components, mock content patterns, and visual language already established by Home and Services.

Implement **only `/services/:serviceId`** in this pass.

After completing Service Detail, STOP.

Do not fully implement Booking, Specialist Detail, or any other placeholder route.

---

# 1. Page Goal

The page should help a visitor who selected a service answer:

1. این خدمت چیست و چه نتیجه‌ای دارد؟
2. حدوداً چقدر زمان و هزینه نیاز دارد؟
3. قبل از رزرو چه نکات مفیدی باید بدانم؟
4. چه متخصصانی می‌توانند این خدمت را ارائه دهند؟
5. چطور همین خدمت را رزرو کنم؟

Primary CTA:

**رزرو این خدمت** → `/book`

The page should convert service discovery into a confident booking decision without becoming a long marketing landing page.

---

# 2. Preserve Existing Foundation

Preserve the current approved implementation and visual system:

- Persian-first UI
- native RTL direction
- Vazirmatn
- Warm Luxury design direction
- existing Public Header/Footer
- warm neutral palette
- restrained Muted Rose accent
- semantic design tokens
- established spacing/radius/shadow system
- Persian display digits
- Toman formatting
- English technical routes
- current responsive patterns
- UI polish already applied to Home and Services

Do not redesign global navigation, shared layouts, buttons, cards, or the design system during this pass.

---

# 3. Required Page Structure

Use this hierarchy:

1. Public Header
2. Breadcrumb / Back-to-Services Context
3. Service Hero / Summary
4. Service Overview
5. Key Information / What to Expect
6. Suitable Specialists
7. Preparation / Important Notes
8. Related Services
9. Final Booking CTA
10. Public Footer

Small compositional adjustments are allowed when they improve hierarchy or responsive behavior.

Do not invent unrelated marketing sections.

---

# 4. Dynamic Service Context

The route is dynamic:

`/services/:serviceId`

The implementation should visibly support different service IDs/slugs rather than behaving as a single hard-coded landing page.

Use deterministic Persian prototype content and reuse the service concepts already present in the application where practical.

Do NOT spend this pass restructuring or consolidating the entire mock-data architecture.

Do NOT create a backend or database.

If an unknown service ID is encountered, use a simple safe fallback appropriate to the existing prototype rather than building a complex error system.

---

# 5. Breadcrumb / Navigation Context

Provide lightweight navigation context such as:

`خدمات / رنگ و لایت`

The user must be able to return to `/services` easily.

Requirements:

- correct RTL order
- correct directional icon behavior
- visually secondary to the service content
- keyboard accessible

Do not introduce a new navigation system.

---

# 6. Service Hero / Summary

Immediately communicate the selected service.

Recommended content:

- service name
- category
- concise natural Persian description
- representative service/result image
- approximate duration
- starting price or price range
- primary booking CTA

Example presentation:

**رنگ و لایت**

`از ۱٬۲۵۰٬۰۰۰ تومان`

`۹۰ تا ۱۲۰ دقیقه`

Primary CTA:

**رزرو این خدمت** → `/book`

Use an editorial composition consistent with Warm Luxury.

Do not create an oversized decorative hero that pushes useful information far below the fold.

Do not add fake badges, ratings, popularity, scarcity, or promotional labels.

---

# 7. Service Overview

Explain the selected service in concise, natural Persian.

Cover useful customer-facing information such as:

- what the service generally includes
- intended cosmetic result/use case
- meaningful variations where relevant

Keep this focused on helping the customer decide.

Do not turn the section into a long SEO article.

Do not make medical, guaranteed-result, or unsupported superiority claims.

---

# 8. Key Information / What to Expect

Present decision-relevant information in a compact scan-friendly composition.

Include where relevant:

- approximate duration
- starting price / price range
- a short explanation when final price can vary
- general appointment expectation

For services such as hair coloring, it is acceptable to explain briefly that price may vary based on factors such as hair length, volume, complexity, or selected technique.

Use honest prototype wording rather than false precision.

Do not invent salon policies that have not been defined.

---

# 9. Pricing Rules

Use Persian digits and Toman.

Prefer:

- `از ... تومان`
- a clear representative range

Do not introduce:

- discounts
- crossed-out prices
- limited-time promotions
- fake packages
- urgency
- scarcity

---

# 10. Duration Rules

Use customer-friendly approximate duration such as:

- `حدود ۶۰ دقیقه`
- `۹۰ تا ۱۲۰ دقیقه`

Do not imply exact operational scheduling guarantees.

---

# 11. Suitable Specialists

Show approximately **2–3 representative specialists** suitable for the selected service where appropriate.

Each preview may contain:

- Persian name
- portrait
- specialty/focus
- concise relevant descriptor
- link toward the existing specialist-detail placeholder where available
- booking entry where useful

Do not fully implement Specialist Detail.

Do not fabricate:

- star ratings
- review counts
- awards
- popularity rankings
- fake credentials

This section should help the visitor understand that specialist choice is part of the booking experience, not recreate the full Specialists page.

---

# 12. Preparation / Important Notes

Where genuinely useful, provide a short practical preparation section.

Use neutral, non-medical guidance appropriate to the selected beauty service.

Keep it concise.

Do not invent:

- cancellation policies
- deposit policies
- medical requirements
- strict operational rules

If a service does not need meaningful preparation guidance, omit the section rather than filling it with generic content.

---

# 13. Related Services

Show approximately **2–3 genuinely related services**.

Examples:

- رنگ و لایت → بالیاژ / تراپی مو / براشینگ
- مانیکور → ژلیش / پدیکور

Keep related items lightweight.

They should route into the existing Service Detail pattern.

Do not build personalization or recommendation logic.

Do not duplicate the full Services catalog.

---

# 14. Booking Context

The primary CTA should clearly communicate that the selected service is the service the user intends to book:

**رزرو این خدمت**

Route to:

`/book`

Do not implement real state persistence, backend booking state, or a complex selected-service transfer mechanism during this Base44 pass.

Structure the UI naturally so this context can be formalized later during local/Codex/backend implementation.

---

# 15. Final Booking CTA

End with one clear conversion section consistent with the existing public pages.

Primary action:

**رزرو این خدمت** → `/book`

Keep CTA hierarchy intentional.

Do not create several competing primary booking actions near each other.

---

# 16. Asset Direction

Use imagery meaningfully related to the selected service/result.

Preserve existing asset conventions where suitable.

Do not spend generation effort repeatedly polishing non-blocking asset inconsistencies.

Do not redesign the site's image system during this pass.

Broken/missing or clearly inappropriate imagery can be captured later in the UI refinement backlog.

---

# 17. Persian / RTL Requirements

Preserve the established locale baseline:

- natural Persian copy
- RTL-native composition
- Vazirmatn
- Persian display digits
- Toman pricing
- correct RTL directional icons
- intentional handling of mixed Persian/English values
- English technical route paths

Do not solve RTL through text alignment alone.

Do not add a language switcher.

---

# 18. Warm Luxury Direction

The page should feel:

- elegant
- calm
- informative
- premium
- visually confident
- conversion-focused

Prefer:

- editorial image/content composition
- strong information hierarchy
- controlled whitespace
- warm neutral surfaces
- restrained Muted Rose accents
- subtle borders
- selective card usage
- minimal shadows

Avoid:

- marketplace/product-store aesthetics
- excessive cards
- excessive badges
- fake-luxury decoration
- heavy gradients
- glassmorphism
- giant pills
- decorative motion
- generic SaaS styling

---

# 19. Responsive Implementation

## Mobile

- service identity must remain immediately clear
- price, duration, and booking CTA must be easy to scan
- hero content should stack naturally
- avoid overly small metadata
- specialist previews must remain touch-friendly
- related services must not create awkward overflow
- preserve comfortable Persian reading width

## Tablet

Use width intentionally and preserve the relationship between imagery and decision information.

## Desktop

Use editorial composition rather than stretching mobile sections.

Keep service identity and booking information visually dominant.

---

# 20. Accessibility

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

# 21. UI Debt Policy

Implement the page cleanly, but do not spend repeated Base44 cycles on non-blocking polish.

After generation, the page will be reviewed for:

- hero balance
- CTA prominence
- information density
- image consistency
- specialist-card consistency
- mobile typography
- spacing rhythm
- accent/supporting-text contrast
- related-service layout
- RTL breadcrumb/directional behavior

Non-blocking issues will be logged for the later local/Codex refinement phase.

---

# 22. Explicitly Out of Scope

Do NOT implement:

- Booking page beyond its existing placeholder
- Specialist Detail beyond its existing placeholder
- backend/database
- real booking persistence
- real availability
- payment
- authentication changes
- pricing engine
- reviews/ratings
- promotions
- recommendation engine
- personalization
- medical guidance
- admin functionality
- architecture/data-model refactoring
- new routes
- dark mode
- full i18n platform

---

# 23. Definition of Done

Service Detail v0.1 is complete when:

- `/services/:serviceId` is implemented beyond placeholder state
- the page responds coherently to the selected service ID/slug
- selected service identity is immediately clear
- price and duration context are visible
- service explanation is useful but concise
- suitable specialist previews are represented where appropriate
- preparation notes are used only where meaningful
- related services support continued discovery without recreating the catalog
- primary booking CTA clearly routes to `/book`
- no fake ratings, promotions, scarcity, or unsupported claims are introduced
- Persian/RTL foundation remains intact
- Warm Luxury remains consistent with Home and Services
- existing UI polish is preserved
- responsive behavior is intentional
- accessibility basics are preserved
- no unrelated pages/features are implemented

Then STOP.

Do not implement Booking, Specialist Detail, or another page.

Wait for review and the next prompt.
