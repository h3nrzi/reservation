# Base44 Foundation Pass — Salon Booking Platform

**Prompt Version:** 0.2  
**Generation Strategy:** Fresh foundation from scratch  
**Primary Locale:** Persian (`fa`)  
**Direction:** RTL

Build the application foundation from scratch for a premium Persian women's beauty salon booking platform.

This is **Foundation Pass v0.2**.

Do NOT treat this as a translation or correction of an English/LTR application. The generated foundation must be Persian-first and RTL-native from the beginning.

Do NOT fully design or implement individual pages yet.

The purpose of this pass is to establish:

- the complete approved route structure
- Persian-first UI foundation
- native RTL behavior
- five reusable layout families
- navigation skeletons
- placeholder pages
- responsive application shells
- design tokens
- Tailwind/styling foundation
- Persian typography
- representative locale formatting

After completing this foundation, STOP.

Do not continue into full page implementation.

---

# 1. Product Context

The product is a beauty salon booking platform for Persian-speaking users, initially oriented toward the Iranian market.

It has two major product surfaces:

1. Customer Experience
2. Salon Management System

The primary customer goal is to discover salon services and specialists and book appointments online without needing phone or in-person scheduling.

The management experience will eventually allow salon staff to manage appointments, customers, services, specialists, schedules, gallery content, and salon settings.

The prototype will initially use deterministic dummy/mock data.

Do not build a production backend, database, real authentication, payment integration, notification infrastructure, or scheduling engine during this pass.

---

# 2. Persian-First Requirement

All user-facing content in this foundation must be natural Persian.

This includes representative:

- navigation labels
- page titles
- buttons
- form labels
- placeholders
- booking-step labels
- admin navigation
- status labels
- sample dates
- sample times
- sample prices
- minimal dummy content

Do not generate an English UI and then right-align it.

Engineering identifiers should remain English where appropriate, including component names, variables, route implementation identifiers, and code architecture.

Technical URL paths must remain in English.

Do NOT create a language switcher.

Do NOT build a full translation-management or internationalization platform during this pass.

This product is Persian-first, not currently a multilingual product.

---

# 3. Native RTL Foundation

The application must be RTL-native from the application/layout level.

Use proper RTL document/application direction semantics rather than simulating RTL through text alignment.

RTL behavior must be correct for:

- public navigation
- headers
- admin sidebar
- breadcrumbs
- booking stepper/progress
- tabs
- drawers
- modals
- pagination
- forms
- tables
- calendar navigation
- previous/next actions
- chevrons and directional arrows
- responsive navigation

Mirror directional UI where semantics require it.

Do not blindly mirror non-directional icons.

Where supported by the generated stack, prefer logical layout concepts such as `start` and `end` instead of unnecessary hard-coded `left` and `right` assumptions.

The desktop Admin sidebar should be positioned on the **right**.

---

# 4. Required Routes

Create exactly these 23 planned routes/pages.

Do not invent additional product routes.

## Public / Booking

1. `/` — خانه
2. `/services` — خدمات
3. `/services/:serviceId` — جزئیات خدمت
4. `/specialists` — متخصصان
5. `/specialists/:specialistId` — پروفایل متخصص
6. `/gallery` — گالری
7. `/book` — رزرو نوبت
8. `/book/confirmation` — تأیید رزرو
9. `/faq` — سوالات متداول

## Customer

10. `/appointments` — نوبت‌های من
11. `/appointments/:appointmentId` — جزئیات نوبت

## Salon Management

12. `/admin/login` — ورود مدیریت
13. `/admin` — داشبورد
14. `/admin/calendar` — تقویم
15. `/admin/appointments` — نوبت‌ها
16. `/admin/appointments/:appointmentId` — جزئیات نوبت
17. `/admin/customers` — مشتریان
18. `/admin/customers/:customerId` — جزئیات مشتری
19. `/admin/services` — مدیریت خدمات
20. `/admin/specialists` — مدیریت متخصصان
21. `/admin/specialists/:specialistId` — جزئیات متخصص
22. `/admin/gallery` — مدیریت گالری
23. `/admin/settings` — تنظیمات

Every route must exist after this pass.

Each route should contain only enough Persian placeholder content to identify and verify the page, layout, direction, and locale behavior.

Do NOT fully design these pages yet.

---

# 5. Non-Route Experiences

Do NOT create separate routes for the following experiences.

## Booking Steps

The `/book` route will eventually contain these internal steps:

1. انتخاب خدمات
2. انتخاب متخصص
3. تاریخ و زمان
4. اطلاعات مشتری
5. مرور رزرو
6. تأیید

These are steps inside `/book`, not independent routes.

For this foundation pass, create only enough structure to demonstrate an RTL multi-step booking shell.

Do not implement the complete booking flow yet.

## Public Content

About and Contact should not receive dedicated routes.

They will eventually exist as sections within the public experience and/or footer.

## Service Management

- Create Service → Drawer
- Edit Service → Drawer
- Delete Service → Confirmation Modal

Do not create separate routes.

## Specialist Management

- Create Specialist → Drawer
- Edit Specialist → Drawer
- Delete Specialist → Confirmation Modal

Do not create separate routes.

## Specialist Detail

The following will eventually be tabs inside `/admin/specialists/:specialistId`:

- پروفایل
- خدمات
- برنامه کاری
- مرخصی / عدم حضور

Do not create separate routes for these tabs.

## Settings

The following will eventually be tabs/sections inside `/admin/settings`:

- اطلاعات سالن
- ساعات کاری
- قوانین رزرو
- اعلان‌ها

Do not create separate settings routes.

---

# 6. Layout Families

Create exactly five reusable layout families.

## Public Layout

Used by public salon discovery pages.

Create only the reusable shell needed for future:

- RTL header/navigation
- main content
- footer
- responsive behavior

It should feel spacious and premium but remain a foundation, not a finished marketing page.

## Booking Layout

Used by:

- `/book`
- `/book/confirmation`

This layout should be focused and distraction-light.

It must support a future RTL multi-step booking experience.

## Customer Layout

Used for customer appointment management.

Keep it simple and suitable for lightweight customer self-service.

## Admin Auth Layout

Used by `/admin/login`.

Keep it separate from the operational Admin shell.

## Admin Layout

Used by salon management routes.

Establish a reusable RTL operational shell with:

- right-side desktop sidebar
- header
- main content area
- responsive navigation behavior

Do not build route-specific dashboard widgets or operational features yet.

---

# 7. Design Direction — Warm Luxury

Use this approved design direction:

> A warm, editorial luxury salon experience for customers, paired with a calm and highly functional operational interface for salon staff.

Brand personality:

- Elegant
- Warm
- Calm
- Premium
- Trustworthy
- Modern

For Persian UI, create the premium/editorial feeling through typography hierarchy, scale, whitespace, composition, photography readiness, and restrained styling.

Do not depend on a Latin editorial font to communicate luxury.

Customer surfaces should feel spacious, visual, calm, and aspirational.

Admin surfaces should belong to the same visual family but be more compact, functional, and efficient.

Do NOT interpret luxury as excessive decoration.

---

# 8. Visual Anti-Patterns

Avoid:

- excessive pink
- excessive gold
- glassmorphism
- gradient-heavy UI
- excessive shadows
- putting everything inside cards
- giant rounded pills everywhere
- decorative animation
- generic SaaS dashboard styling
- fake-luxury styling
- low-contrast premium aesthetics
- excessive decoration inside booking

Prefer whitespace, typography, hierarchy, subtle borders, and deliberate composition before decorative effects.

---

# 9. Primitive Color Tokens

Establish these primitive colors centrally.

## Warm Neutral

- `warm-50` → `#FCFAF7`
- `warm-100` → `#F7F2EC`
- `warm-200` → `#EDE4DA`
- `warm-300` → `#DDCFC1`
- `warm-400` → `#BDAA98`
- `warm-500` → `#9B8775`
- `warm-600` → `#796757`
- `warm-700` → `#5E4E41`
- `warm-800` → `#44372F`
- `warm-900` → `#2E2520`
- `warm-950` → `#1D1714`

## Muted Rose

- `rose-50` → `#FCF7F7`
- `rose-100` → `#F8EEEE`
- `rose-200` → `#EFDADA`
- `rose-300` → `#E1BCBE`
- `rose-400` → `#CD969B`
- `rose-500` → `#B8757D`
- `rose-600` → `#9E5963`
- `rose-700` → `#83464F`
- `rose-800` → `#6D3C44`
- `rose-900` → `#5C353C`
- `rose-950` → `#321A1F`

Muted Rose is a restrained brand accent.

Do not make the application predominantly pink.

---

# 10. Semantic Color Layer

Application components should prefer semantic tokens instead of directly coupling to primitive palette values.

Establish semantic tokens equivalent to:

- `background` → warm-50
- `foreground` → warm-950
- `surface` → white
- `surface-subtle` → warm-100
- `surface-elevated` → white
- `primary` → rose-700
- `primary-hover` → rose-800
- `primary-foreground` → white
- `secondary` → warm-200
- `secondary-foreground` → warm-900
- `muted` → warm-100
- `muted-foreground` → warm-600
- `border` → warm-200
- `border-strong` → warm-300
- `input` → warm-200
- `ring` → rose-500

Also establish independent accessible semantic states for:

- success
- warning
- danger
- info

Do not use brand Rose as the error color merely because it exists.

Architecture should follow:

Primitive Tokens  
→ Semantic Tokens  
→ Component Variants  
→ UI

Avoid scattered raw hex values throughout page components.

---

# 11. Persian Typography

Use **Vazirmatn** as the primary user-facing typeface.

Use it for:

- Persian headings
- body copy
- navigation
- buttons
- forms
- booking controls
- tables
- labels
- admin UI

Do not use Cormorant Garamond for Persian headings.

Do not introduce another Persian display font during this foundation pass.

Create visual hierarchy through scale and weight.

Initial type scale:

- xs → 12px
- sm → 14px
- base → 16px
- lg → 18px
- xl → 20px
- 2xl → 24px
- 3xl → 30px
- 4xl → 36px
- 5xl → 48px
- 6xl → 60px

Persian typography must use comfortable line-height. Do not blindly copy tight Latin heading/body line heights.

Admin UI should generally remain between `sm` and `2xl`.

---

# 12. Persian Numerals

Use Persian digits for representative user-facing display content.

Examples:

- `۱۲`
- `۱۴۰۵`
- `۰۹:۳۰`
- `۱٬۲۵۰٬۰۰۰ تومان`

Do not assume displayed values and future stored/domain values are identical.

Phone numbers, URLs, IDs, emails, and technical values may require controlled LTR/bidi behavior.

Do not blindly transform every numeric input into Persian digits.

---

# 13. Calendar & Date Direction

The user-facing calendar system is **Jalali / Solar Hijri**.

The future booking date picker and admin calendar must be designed for Jalali/Persian presentation.

During this foundation pass, do not build a complete calendar engine or scheduling algorithm.

However, representative placeholder dates should demonstrate the intended locale.

Examples may resemble:

- `شنبه ۱۵ آذر`
- `۱۵ آذر ۱۴۰۵`

Do not use US month/day formatting.

Do not hard-code a future backend date storage strategy into the frontend foundation.

---

# 14. Time

Use 24-hour time for representative UI.

Examples:

- `۰۹:۳۰`
- `۱۷:۰۰`

This applies especially to booking and admin/calendar contexts.

---

# 15. Currency

Use **Toman (تومان)** for representative customer-facing prices.

Example:

`۱٬۲۵۰٬۰۰۰ تومان`

Use readable thousands separators.

Do not scatter money-formatting logic across components.

Do not decide backend monetary storage during this pass.

---

# 16. Radius

Use:

- small → 6px
- medium → 10px
- large → 16px
- extra-large → 24px
- full → 9999px

Initial guidance:

- Button → medium
- Input → medium
- Card → large
- Modal → large / extra-large
- Badge → full

Do not use pill radius everywhere.

---

# 17. Shadows & Surfaces

Keep shadows restrained.

Support approximately:

- small
- medium
- large

Prefer:

Whitespace + hierarchy + subtle border

before:

Shadow

Medium/large shadows are primarily appropriate for elevated UI such as:

- dropdowns
- popovers
- drawers
- modals

Ordinary content cards should not all appear to float.

---

# 18. Spacing & Layout

Preserve the standard Tailwind spacing scale unless a real project need requires otherwise.

Use these semantic layout values:

- mobile page gutter → 16px
- tablet page gutter → 24px
- desktop page gutter → 32px
- mobile section gap → 64px
- desktop section gap → 96px
- primary content max width → 1280px
- reading max width → 720px

Admin:

- sidebar width → 256px
- header height → 64px
- content → fluid where operationally useful

RTL changes directional placement, not these spacing magnitudes.

---

# 19. Control Density

Support:

- small control → 36px
- medium control → 44px
- large control → 52px

Guidance:

- Customer → medium / large
- Booking → medium / large
- Admin → small / medium

Customer and Admin should share one design system while supporting different density levels.

Ensure Persian labels fit naturally. Do not size components based only on English text assumptions.

---

# 20. Responsive Foundation

Use standard Tailwind breakpoints initially.

Do not invent custom breakpoints unless demonstrated need appears later.

Customer experience:

- mobile-first
- spacious on desktop
- desktop must not look like enlarged mobile UI

Admin experience:

- explicitly desktop-aware
- right-side desktop navigation
- responsive navigation on smaller screens
- future Calendar UI must be able to use desktop width efficiently

Test the structural foundation with Persian text lengths and RTL flow.

---

# 21. Mixed RTL/LTR Content

The Persian UI will sometimes contain LTR fragments such as:

- phone numbers
- email addresses
- URLs
- IDs
- technical codes

Handle bidi/mixed-direction content intentionally so values remain readable and do not visually reorder surrounding Persian text incorrectly.

Do not attempt to make technical URLs or engineering identifiers Persian.

---

# 22. Interaction States

Foundation components must support the concept of:

- default
- hover
- active
- focus
- disabled
- selected
- loading

Focus must remain clearly visible.

Initial guidance:

- focus ring → 2px
- focus offset → 2px

Keyboard/focus order must remain logical for RTL experiences.

Do not sacrifice accessibility for premium styling.

---

# 23. Dark Mode

Do NOT implement dark mode in this version.

Keep semantic token architecture clean enough that another theme could be introduced later.

---

# 24. Foundation Components

Create only the minimum reusable primitives necessary to establish and verify the foundation.

Examples may include:

- Button
- Input
- navigation primitives
- layout primitives
- placeholder surface/container
- basic status/badge treatment if needed

Do NOT build a large component library yet.

Do NOT create complex product-specific components yet.

---

# 25. Dummy Data

The later frontend prototype will use deterministic Persian dummy/mock data.

For this Foundation Pass, use only minimal natural Persian examples required to verify routes, RTL, typography, and locale presentation.

Do not populate pages with extensive fake content yet.

Do not use obviously translated English demo names/content.

---

# 26. Explicitly Out of Scope

Do NOT build during this pass:

- backend
- database
- real authentication
- real authorization
- payment integration
- notification delivery
- scheduling algorithm
- availability engine
- production API
- full booking flow
- full admin CRUD
- analytics
- waitlist
- reviews
- loyalty
- memberships
- gift cards
- referral system
- promotions
- advanced reports
- language switcher
- full localization management platform
- dark mode

Do not generate features simply because they are common in salon applications.

---

# 27. Tailwind / Styling Rules

The styling foundation should:

1. Preserve useful Tailwind defaults where no project-specific decision exists.
2. Centralize approved primitive and semantic tokens.
3. Prefer semantic tokens in application components.
4. Avoid scattered raw hex values.
5. Avoid direct primitive coupling where semantic meaning exists.
6. Avoid arbitrary values when an approved token or standard scale is appropriate.
7. Prefer logical RTL-aware styling over unnecessary physical left/right assumptions.
8. Establish RTL globally/layout-level rather than through ad-hoc component patches.
9. Support customer, booking, and admin density differences deliberately.
10. Keep engineering identifiers and route paths in English.

---

# 28. Definition of Done

Foundation Pass v0.2 is complete only when:

- all 23 required routes exist
- no extra product routes were invented
- all route placeholders use natural Persian user-facing labels
- technical route paths remain English
- five layout families exist
- the application is genuinely RTL-native
- Public Layout is RTL
- Booking Layout is RTL
- Customer Layout is RTL
- Admin Auth Layout is RTL
- Admin Layout is RTL
- desktop Admin sidebar is on the right
- appropriate navigation skeletons exist
- responsive shells exist
- Vazirmatn is the primary Persian UI typeface
- representative UI uses Persian digits
- representative date presentation is Jalali/Persian
- representative time uses 24-hour formatting
- representative prices use Toman
- mixed RTL/LTR content is considered
- directional icons/actions behave correctly
- Warm Luxury direction is reflected in the foundation
- primitive colors exist
- semantic tokens exist
- radius/shadow/spacing foundations exist
- customer/admin density differences are supported
- styling avoids the listed anti-patterns
- no production backend was created
- no full page implementation was performed
- no unnecessary language switcher/i18n platform was created

Then STOP.

Do not continue designing the Home page or any other individual page.

Wait for review and the next prompt.

---

# Final Instruction

Generate this as a fresh Persian/RTL foundation from the beginning.

Do not reproduce an English/LTR foundation first and then patch or translate it.

The first rendered experience should already demonstrate the intended Persian language, RTL direction, Persian typography, and locale conventions.
