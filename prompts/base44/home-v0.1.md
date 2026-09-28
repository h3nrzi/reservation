# Base44 Page Implementation — Home

**Prompt Version:** 0.1  
**Target Route:** `/`  
**Scope:** Home page only  
**Locale:** Persian-first / RTL-native  
**Design Direction:** Warm Luxury

Implement the Home page of the existing Persian beauty salon booking application.

This is a **page implementation pass**, not a new foundation pass.

Use the existing approved application foundation, routes, layouts, design tokens, RTL behavior, and styling system. Do not rebuild or replace the global foundation unless a genuine implementation defect prevents this page from working correctly.

Implement **only the `/` Home page** in this pass.

After completing the Home page, STOP.

Do not proceed to fully implement any other route.

---

# 1. Page Goal

The Home page should help a visitor quickly understand:

- this is a premium women's beauty salon
- what kinds of services are available
- that customers can choose specialists
- that appointments can be booked online
- that the salon's work can be evaluated visually
- how to begin booking

The primary conversion goal is to move qualified visitors into the booking flow.

Primary CTA:

**رزرو نوبت** → `/book`

Secondary CTA:

**مشاهده خدمات** → `/services`

Every major section should primarily contribute to at least one of:

- Discovery
- Trust
- Conversion

Do not add sections simply because they are common on marketing websites.

---

# 2. Preserve Existing Foundation

Preserve the approved Foundation v0.2 decisions:

- Persian-first UI
- native RTL direction
- Vazirmatn typography
- Warm Luxury design direction
- warm neutral palette
- restrained Muted Rose accent
- semantic design tokens
- approved radius/shadow/spacing system
- Persian numeral presentation
- Toman price presentation
- 24-hour time where relevant
- Jalali/Persian dates where relevant
- English technical route paths
- existing Public Layout

Do not introduce a separate visual system for Home.

Do not convert the project back to LTR or English.

---

# 3. Required Home Structure

Implement the Home page using this hierarchy:

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

Small compositional adjustments are allowed when they improve visual hierarchy or responsive behavior.

Do not invent major additional sections.

---

# 4. Header

Use and refine the existing Public Layout header rather than creating a disconnected Home-only navigation system.

Representative navigation:

- خانه
- خدمات
- متخصصان
- گالری
- سوالات متداول

Primary header action:

**رزرو نوبت** → `/book`

Requirements:

- RTL-native
- responsive
- clear active/current-page treatment where appropriate
- uncluttered
- visually consistent with Warm Luxury

Do not overcrowd the header.

---

# 5. Hero

Create a strong, spacious Persian hero that communicates the salon positioning and makes online booking immediately obvious.

Use concise, natural Persian copy.

Avoid generic machine-translated marketing phrases and exaggerated/unverifiable claims.

Do not claim things such as "بهترین سالن ایران".

Required actions:

Primary:

**رزرو نوبت** → `/book`

Secondary:

**مشاهده خدمات** → `/services`

Visual direction:

- premium beauty/salon photography should have a meaningful role
- editorial composition
- generous whitespace
- strong Persian typographic hierarchy
- restrained color usage
- excellent text contrast

Do not use generic SaaS illustrations.

Do not place Persian copy over visually noisy imagery if readability suffers.

---

# 6. Featured Services

Show approximately **4–6 representative services**.

Use deterministic Persian dummy data.

Suitable examples include:

- رنگ و لایت
- کوتاهی و استایل مو
- میکاپ
- خدمات ناخن
- ابرو و مژه
- مراقبت و زیبایی مو

Each preview may include useful summary information such as:

- service name
- short natural Persian description
- representative duration
- representative starting price
- relevant image where useful

Use Persian digits and Toman formatting.

Example formatting:

`از ۱٬۲۵۰٬۰۰۰ تومان`

Do not build the full service catalog on Home.

Provide a clear route to `/services` and service details where appropriate.

---

# 7. Why Ara

Create a concise value-proposition section.

Focus on a small number of meaningful benefits, such as:

- انتخاب متخصص متناسب با خدمت
- مشاهده زمان‌های قابل رزرو
- رزرو آنلاین ساده و شفاف
- تمرکز بر کیفیت و تجربه حرفه‌ای

Avoid generic filler.

Avoid turning this into a large grid of repetitive cards.

Do not fabricate quantitative claims.

---

# 8. Featured Specialists

Show approximately **3 representative specialists** using deterministic Persian dummy data.

Each specialist preview may contain:

- natural Persian name
- specialty / focus
- portrait
- short useful descriptor
- link to specialist profile
- booking entry where appropriate

Provide access to `/specialists`.

Do NOT invent fake ratings, review counts, awards, or popularity statistics.

---

# 9. Portfolio / Gallery Preview

Create an image-led preview of salon work.

The goal is visual trust, not decoration.

Use representative imagery appropriate to actual salon/beauty work.

Prefer an editorial image composition over a repetitive card grid where appropriate.

Provide access to `/gallery`.

Do not duplicate the complete Gallery page.

Do not use irrelevant lifestyle imagery solely to fill space.

---

# 10. How Booking Works

Explain online booking in approximately **3 simple conceptual stages**:

1. خدمت و متخصص را انتخاب کنید
2. زمان مناسب را پیدا کنید
3. اطلاعات را تأیید و نوبت را ثبت کنید

This section should reduce uncertainty, not reproduce the complete six-step booking interface.

The visual sequence must read naturally in RTL.

Keep the copy concise and task-oriented.

A CTA may lead to `/book`.

---

# 11. Trust / Social Proof

Create trust without fabricating evidence.

Do NOT invent:

- customer review counts
- star ratings
- customer totals
- awards
- press logos
- years-in-business claims
- verified testimonials
- success percentages

Build trust through the product and content itself:

- professional specialist presentation
- clear service information
- high-quality portfolio presentation
- transparent booking explanation
- thoughtful salon/quality messaging

If prototype testimonial-like content is used for visual exploration, it must not be presented as verified real-world evidence.

Prefer avoiding fabricated testimonial content entirely if the section works without it.

---

# 12. FAQ Preview

Show approximately **3–4 concise questions**.

Representative topics:

- چطور نوبت رزرو کنم؟
- آیا می‌توانم متخصص موردنظرم را انتخاب کنم؟
- اگر نیاز به تغییر یا لغو نوبت داشته باشم چه کار کنم؟
- چه زمانی باید در سالن حاضر شوم؟

Use concise natural Persian answers.

Provide access to `/faq` for the complete FAQ experience.

Do not overload Home with the full FAQ.

---

# 13. Final Booking CTA

After the visitor has seen the services, specialists, work samples, and booking explanation, provide a strong final conversion section.

Primary action:

**رزرو نوبت** → `/book`

Make the section visually distinct primarily through composition, spacing, typography, and restrained surface treatment.

Avoid heavy gradients and excessive decoration.

---

# 14. Footer

Use/refine the existing Public Layout footer.

It may include concise access to:

- public navigation
- salon/contact placeholders
- About/Contact content where appropriate
- booking CTA

Do not create new About or Contact routes.

Do not invent real business contact information if it has not been provided.

---

# 15. Dummy Data

Use a small, deterministic Persian dummy-data set for this page.

Prefer reusable data structures instead of scattering arbitrary literals throughout components.

Use natural Persian examples for:

- services
- specialists
- descriptions
- durations
- prices
- FAQ

Do not create a backend or database.

Do not over-engineer the data layer for a single page.

---

# 16. Persian / RTL Requirements

The completed Home page must be Persian-first and RTL-native.

Requirements:

- natural Persian user-facing copy
- `dir="rtl"` / correct application-level RTL semantics inherited from foundation
- Vazirmatn
- Persian digits for normal display values
- Toman price formatting
- correct RTL directional icons
- intentional handling of any mixed RTL/LTR values
- English technical routes

Do not solve RTL by merely applying `text-align: right`.

Do not add a language switcher.

---

# 17. Warm Luxury Design Direction

The Home page should feel:

- elegant
- warm
- calm
- premium
- modern
- visual
- spacious

Prefer:

- generous whitespace
- strong Persian typographic hierarchy
- warm neutral surfaces
- restrained Muted Rose accents
- subtle borders
- minimal shadows
- selective card usage
- editorial/image-led compositions

Avoid:

- excessive pink
- excessive gold
- glassmorphism
- gradient-heavy UI
- excessive shadows
- card-everything layouts
- giant pills everywhere
- generic SaaS aesthetics
- fake-luxury styling
- decorative motion
- low-contrast text

---

# 18. Responsive Implementation

Implement intentional responsive behavior rather than simply shrinking desktop UI.

## Mobile

- keep the primary booking CTA prominent
- use an appropriate responsive navigation pattern
- preserve readable Persian line lengths
- keep touch targets comfortable
- adapt imagery without destructive cropping
- avoid horizontal overflow
- allow sections/cards to stack naturally

## Tablet

Use available width deliberately and avoid treating tablet as enlarged mobile.

## Desktop

Use editorial composition, whitespace, and meaningful multi-column/image layouts where appropriate.

Do not render desktop as a stretched mobile page.

Respect the approved content width system while allowing intentional visual sections to extend wider where appropriate.

---

# 19. Interaction & Accessibility

Use subtle, purposeful interaction feedback.

Support:

- hover
- focus
- active
- keyboard navigation
- adequate touch targets

Maintain:

- sufficient contrast
- meaningful heading hierarchy
- visible focus states
- useful image alt text
- keyboard-accessible buttons/links
- readable Persian typography
- non-color-only communication

Do not sacrifice usability for premium aesthetics.

---

# 20. Scope Guardrails

Do NOT implement during this Home pass:

- other pages beyond what is minimally necessary for existing navigation links
- production backend
- database
- authentication
- booking logic
- dynamic availability
- payments
- notifications
- reviews/ratings system
- loyalty
- promotions
- memberships
- waitlist
- recommendation engine
- analytics
- new routes
- full i18n system
- dark mode

Do not redesign the global foundation simply because a different design could also work.

---

# 21. Definition of Done

Home v0.1 is complete only when:

- `/` is fully implemented beyond the placeholder state
- the approved Home hierarchy is represented
- the Hero clearly communicates the product and booking action
- `رزرو نوبت` is the clear primary CTA
- service discovery is useful without duplicating `/services`
- specialist discovery is useful without duplicating `/specialists`
- Gallery preview provides visual evidence and routes deeper
- How Booking Works is concise and RTL-aware
- trust is created without fabricated claims
- FAQ remains a preview rather than a full duplicate
- final booking CTA exists
- page is fully Persian-first
- page is genuinely RTL-native
- Vazirmatn and approved design tokens are preserved
- dummy data is natural Persian and deterministic
- representative prices use Persian digits and Toman
- responsive behavior is intentional across mobile, tablet, and desktop
- accessibility basics are preserved
- no unrelated routes/features were invented
- the existing Foundation v0.2 remains intact

Then STOP.

Do not implement `/services`, `/specialists`, `/gallery`, `/book`, or any other page beyond their existing foundation placeholders.

Wait for review and the next page prompt.
