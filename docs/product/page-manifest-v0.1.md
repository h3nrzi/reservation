# Salon Booking Platform — Page Manifest

**Version:** 0.1  
**Status:** Approved for Design Foundation

## Purpose

Define the actual route/page foundation that Base44 should create as placeholders before page design begins.

This manifest is derived from the approved core journeys, capability map, MVP boundary, and route/screen classification.

A product step, tab, drawer, modal, or section is intentionally not counted as a page unless independent navigation/deep-link context provides meaningful value.

---

# Classification Rule

Use an independent route/page when the experience benefits from one or more of:

- Direct navigation / deep-linking
- Browser refresh preserving context
- Independent navigation history
- Meaningful standalone context
- Entry from multiple areas of the application

Otherwise prefer a Step, Tab, Drawer, Modal, or Section.

---

# Customer Surface

## Public Routes

### P01 — Home

**Route:** `/`  
**Layout:** Public  
**Initial Base44 State:** Placeholder

Primary salon landing/discovery page.

About and Contact content should initially be sections of the public experience rather than dedicated pages.

### P02 — Services

**Route:** `/services`  
**Layout:** Public  
**Initial Base44 State:** Placeholder

Browse salon services.

### P03 — Service Detail

**Route:** `/services/:serviceId`  
**Layout:** Public  
**Initial Base44 State:** Placeholder

Standalone service information and booking entry point.

### P04 — Specialists

**Route:** `/specialists`  
**Layout:** Public  
**Initial Base44 State:** Placeholder

Browse salon specialists.

### P05 — Specialist Profile

**Route:** `/specialists/:specialistId`  
**Layout:** Public  
**Initial Base44 State:** Placeholder

Standalone specialist profile, capabilities, portfolio context, and booking entry point.

### P06 — Gallery

**Route:** `/gallery`  
**Layout:** Public  
**Initial Base44 State:** Placeholder

Public salon portfolio/gallery.

### P07 — Booking

**Route:** `/book`  
**Layout:** Booking  
**Initial Base44 State:** Placeholder

Booking is one route containing a multi-step flow.

Internal steps:

1. Service Selection
2. Specialist Preference
3. Date & Time / Compatible Availability
4. Customer Details
5. Review
6. Confirm

These steps are not separate pages in v0.1.

### P08 — Booking Confirmation

**Route:** `/book/confirmation`  
**Layout:** Booking  
**Initial Base44 State:** Placeholder

Standalone successful-booking result and next actions.

### P09 — FAQ

**Route:** `/faq`  
**Layout:** Public  
**Initial Base44 State:** Placeholder

Booking and salon questions/policies.

---

# Customer Appointment Routes

### P10 — My Appointments

**Route:** `/appointments`  
**Layout:** Customer  
**Initial Base44 State:** Placeholder

Customer appointment history/upcoming appointments.

Guest/customer identity mechanics will be refined later.

### P11 — Appointment Detail

**Route:** `/appointments/:appointmentId`  
**Layout:** Customer  
**Initial Base44 State:** Placeholder

Appointment details and eligible customer actions such as reschedule/cancel.

---

# Salon Management Surface

### P12 — Admin Login

**Route:** `/admin/login`  
**Layout:** Admin Auth  
**Initial Base44 State:** Placeholder

Management authentication entry point.

### P13 — Dashboard

**Route:** `/admin`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Operational overview. Do not invent dashboard metrics during the foundation pass.

### P14 — Calendar

**Route:** `/admin/calendar`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Primary daily scheduling/operations surface.

### P15 — Appointments

**Route:** `/admin/appointments`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Search/filter/browse appointments beyond calendar context.

### P16 — Appointment Detail

**Route:** `/admin/appointments/:appointmentId`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Standalone appointment management context accessible from calendar, appointment lists, and customer history.

### P17 — Customers

**Route:** `/admin/customers`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Customer directory.

### P18 — Customer Detail

**Route:** `/admin/customers/:customerId`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Customer context and appointment history.

### P19 — Services Management

**Route:** `/admin/services`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Manage service catalog.

Create/Edit Service should initially be a Drawer. Delete confirmation should be a Modal.

### P20 — Specialists Management

**Route:** `/admin/specialists`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Browse/manage specialists.

Create Specialist should initially be a Drawer.

### P21 — Specialist Detail

**Route:** `/admin/specialists/:specialistId`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Specialist management context.

Internal tabs:

- Profile
- Services
- Schedule
- Time Off

Edit actions may use Drawers where appropriate.

### P22 — Gallery Management

**Route:** `/admin/gallery`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

Manage public portfolio/gallery content.

### P23 — Settings

**Route:** `/admin/settings`  
**Layout:** Admin  
**Initial Base44 State:** Placeholder

One settings route with internal tabs/sections rather than separate pages.

Initial areas:

- Salon
- Business Hours
- Booking Rules
- Notifications

---

# Non-Route Experiences

The following must NOT be counted as pages in the Base44 foundation prompt.

## Booking Steps

- Service Selection
- Specialist Preference
- Date & Time
- Customer Details
- Review
- Confirm

**Type:** Step inside `/book`

## Public Content

- About
- Contact

**Type:** Section within public experience / footer as appropriate

## Service Management

- Create Service
- Edit Service

**Type:** Drawer

- Delete Service

**Type:** Confirmation Modal

## Specialist Management

- Create Specialist
- Edit Specialist

**Type:** Drawer

- Delete Specialist

**Type:** Confirmation Modal

## Specialist Detail Areas

- Profile
- Services
- Schedule
- Time Off

**Type:** Tabs inside `/admin/specialists/:specialistId`

## Settings Areas

- Salon
- Business Hours
- Booking Rules
- Notifications

**Type:** Tabs/sections inside `/admin/settings`

---

# Layout Taxonomy v0.1

The Base44 foundation should recognize these layout families:

1. **Public Layout** — public discovery pages
2. **Booking Layout** — focused booking/confirmation experience
3. **Customer Layout** — appointment management experience
4. **Admin Auth Layout** — management authentication
5. **Admin Layout** — salon management application shell

Exact visual design is deferred to Design Tokens and the Base44 foundation prompt.

---

# Page Count

**23 planned routes/pages** for the v0.1 foundation.

Breakdown:

- Public + Booking: 9
- Customer Appointments: 2
- Salon Management: 12

This replaces the earlier 41-item candidate inventory as the approved route/page baseline.

The earlier inventory remains useful as discovery history but must not be used as the Base44 page count.

---

# Base44 Foundation Requirement

The first Base44 foundation pass should:

1. Create all 23 routes.
2. Make every route navigable where appropriate.
3. Create only minimal placeholder content for each route.
4. Establish the five layout families.
5. Establish design tokens / Tailwind foundation from the separate Design Tokens document.
6. Not implement actual page content yet.
7. Not invent additional pages.
8. Stop after the foundation pass for review.

---

# Next Step

Page Manifest v0.1  
→ Design Direction  
→ Design Tokens v0.1  
→ Base44 Foundation Prompt  
→ Foundation Review
