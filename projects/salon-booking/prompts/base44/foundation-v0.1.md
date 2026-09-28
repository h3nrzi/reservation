# Base44 Foundation Pass — Salon Booking Platform

**Prompt Version:** 0.1

Build only the application foundation for a premium women's beauty salon booking platform.

This is **Foundation Pass #1**.

Do NOT fully design or implement the individual pages yet.

The purpose of this pass is to establish:

- the complete route structure
- layout families
- navigation skeletons
- placeholder pages
- responsive application shells
- design tokens
- Tailwind/styling foundation

After completing this foundation, STOP.

Do not continue into full page implementation.

---

# 1. Product Context

The product is a beauty salon booking platform with two major surfaces:

1. Customer Experience
2. Salon Management System

The primary customer goal is to discover salon services and specialists and book appointments online.

The management experience allows salon staff to manage appointments, customers, services, specialists, schedules, gallery content, and salon settings.

This application will initially use dummy/mock data.

Do not build a production backend, database, authentication system, payment integration, or notification infrastructure during this pass.

---

# 2. Required Routes

Create exactly these 23 planned routes/pages.

Do not invent additional pages.

## Public / Booking

1. `/` — Home
2. `/services` — Services
3. `/services/:serviceId` — Service Detail
4. `/specialists` — Specialists
5. `/specialists/:specialistId` — Specialist Profile
6. `/gallery` — Gallery
7. `/book` — Booking
8. `/book/confirmation` — Booking Confirmation
9. `/faq` — FAQ

## Customer

10. `/appointments` — My Appointments
11. `/appointments/:appointmentId` — Appointment Detail

## Salon Management

12. `/admin/login` — Admin Login
13. `/admin` — Dashboard
14. `/admin/calendar` — Calendar
15. `/admin/appointments` — Appointments
16. `/admin/appointments/:appointmentId` — Appointment Detail
17. `/admin/customers` — Customers
18. `/admin/customers/:customerId` — Customer Detail
19. `/admin/services` — Services Management
20. `/admin/specialists` — Specialists Management
21. `/admin/specialists/:specialistId` — Specialist Detail
22. `/admin/gallery` — Gallery Management
23. `/admin/settings` — Settings

Every route must exist after this pass.

Each route should contain only enough placeholder content to identify and verify the page.

Do NOT fully design these pages yet.

---

# 3. Non-Route Experiences

Do NOT create separate pages/routes for the following.

## Booking Steps

The `/book` route will eventually contain:

1. Service Selection
2. Specialist Preference
3. Date & Time
4. Customer Details
5. Review
6. Confirm

These are internal steps, NOT separate routes.

For now, only establish enough structure to show that `/book` is intended to support a multi-step booking flow.

Do not implement the complete booking experience yet.

## Public Content

About and Contact should not receive dedicated routes.

They will eventually exist as sections within the public experience and/or footer.

## Service Management

Create Service → Drawer  
Edit Service → Drawer  
Delete Service → Confirmation Modal

Do not create separate routes.

## Specialist Management

Create Specialist → Drawer  
Edit Specialist → Drawer  
Delete Specialist → Confirmation Modal

Do not create separate routes.

## Specialist Detail

These will eventually be tabs inside `/admin/specialists/:specialistId`:

- Profile
- Services
- Schedule
- Time Off

Do not create routes for these tabs.

## Settings

These will eventually be tabs/sections inside `/admin/settings`:

- Salon
- Business Hours
- Booking Rules
- Notifications

Do not create separate settings routes.

---

# 4. Layout Families

Create five reusable layout families.

## Public Layout

Used by public salon discovery pages.

Establish only the shell required for future header/navigation, content, footer, and responsive behavior.

## Booking Layout

Used by `/book` and `/book/confirmation`.

This layout should feel more focused than the marketing/public experience. Avoid unnecessary distractions.

## Customer Layout

Used for customer appointment management. Keep it simple and appropriate for lightweight customer self-service.

## Admin Auth Layout

Used by `/admin/login`. Separate from the operational Admin shell.

## Admin Layout

Used by salon management routes.

Establish the reusable application shell required for sidebar/navigation, header, main content area, and responsive behavior.

Do not build route-specific dashboard widgets or operational features yet.

---

# 5. Design Direction — Warm Luxury

Use this design direction:

> A warm, editorial luxury salon experience for customers, paired with a calm and highly functional operational interface for salon staff.

Brand personality:

- Elegant
- Warm
- Calm
- Premium
- Trustworthy
- Modern

The customer experience should feel spacious, visual, editorial, and aspirational.

The admin experience should belong to the same visual family but be more compact, functional, and efficient.

Do NOT interpret luxury as excessive decoration.

---

# 6. Anti-Patterns

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
- excessive decoration in the booking flow

Use whitespace, typography, hierarchy, subtle borders, and high-quality structure before decorative effects.

---

# 7. Color Primitives

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

Muted Rose is a restrained accent. Do not make the application predominantly pink.

---

# 8. Semantic Color Layer

Do not couple application components directly to primitive palette values when a semantic token exists.

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

Also establish accessible semantic states for success, warning, danger, and info.

Do not use the brand Rose as the error color merely because it is available.

Architecture should follow:

Primitive Tokens  
→ Semantic Tokens  
→ Component Variants  
→ UI

Avoid hard-coded hex values throughout page components.

---

# 9. Typography

Use:

**Display:** Cormorant Garamond  
**Functional/UI:** Inter

Cormorant Garamond should be used selectively for customer-facing editorial headings.

Do NOT use it for forms, buttons, booking controls, tables, or routine admin UI.

Inter should be the primary functional typeface throughout the application.

Type scale:

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

Admin UI should generally remain between `sm` and `2xl`.

---

# 10. Radius

- small → 6px
- medium → 10px
- large → 16px
- extra-large → 24px
- full → 9999px

Initial guidance:

Button → medium  
Input → medium  
Card → large  
Modal → large / extra-large  
Badge → full

Do not use full/pill radius everywhere.

---

# 11. Shadows & Surfaces

Keep shadows restrained.

Support approximately small, medium, and large shadows.

Prefer whitespace + hierarchy + subtle border before shadow.

Medium/large shadows are primarily appropriate for elevated experiences such as dropdowns, popovers, drawers, and modals.

Ordinary cards should not all appear to float.

---

# 12. Spacing & Layout

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

Calendar and data-heavy admin experiences should eventually be able to use available desktop width.

---

# 13. Control Density

- small control → 36px
- medium control → 44px
- large control → 52px

Guidance:

Customer → medium / large  
Booking → medium / large  
Admin → small / medium

Customer and Admin should share one design system while supporting different density levels.

---

# 14. Responsive Foundation

Use standard Tailwind breakpoints initially.

Do not invent custom breakpoints unless there is demonstrated need.

Customer experience:

- mobile-first
- spacious on desktop
- desktop should not look like enlarged mobile UI

Admin experience:

- must support efficient desktop usage
- navigation should respond appropriately on smaller screens
- future Calendar UI must have room to use desktop space effectively

---

# 15. Interaction States

Foundation components must support the concept of:

- default
- hover
- active
- focus
- disabled
- selected
- loading

Focus should be clearly visible.

Initial guidance:

- focus ring → 2px
- focus offset → 2px

Do not sacrifice accessibility for premium styling.

---

# 16. Dark Mode

Do NOT implement dark mode in this version.

Keep semantic token architecture clean enough that another theme could be introduced later.

---

# 17. Foundation Components

Create only the minimum reusable primitives needed to establish and verify the foundation.

Examples may include:

- Button
- Input
- basic navigation primitives
- basic layout primitives
- basic placeholder surface/container
- basic status/badge treatment if necessary

Do NOT build a large component library yet.

Do NOT create complex product-specific components yet.

---

# 18. Dummy Data

This application will use deterministic dummy/mock data during the frontend prototype phase.

However, this Foundation Pass should NOT build detailed datasets or business logic.

Use only minimal placeholder information necessary to verify routing and layouts.

---

# 19. Explicitly Out of Scope

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

Do not generate these simply because they are common in salon applications.

---

# 20. Definition of Done

Foundation Pass #1 is complete only when:

- all 23 required routes exist
- no extra product routes were invented
- route placeholders are identifiable
- five layout families exist
- appropriate navigation skeletons exist
- responsive shells exist
- Warm Luxury design direction is reflected in the foundation
- primitive colors exist
- semantic tokens exist
- typography foundation exists
- radius/shadow/spacing foundations exist
- customer/admin density differences are supported
- styling avoids the listed anti-patterns
- no production backend was created
- no full page implementation was performed

Then STOP.

Do not continue designing the Home page or any other individual page.

Wait for review and the next prompt.
