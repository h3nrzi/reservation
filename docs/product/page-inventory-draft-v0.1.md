# Salon Booking Platform — Page Inventory

**Version:** 0.1  
**Status:** Draft / Candidate Inventory

## Important

This document is NOT the final Page Manifest.

Items listed here represent candidate screens and product experiences discovered so far.

An item in this document does not automatically imply:

- a dedicated URL
- a React page
- a separate route
- a full-screen experience

Some candidates may eventually become:

- Routes
- Steps
- Tabs
- Modals
- Drawers
- Nested views
- Components

Route and screen decisions will be made after further product discovery.

---

# Customer Experience

## Discovery

### 01 — Home

Primary public landing experience.

Potential responsibilities:

- Introduce salon
- Present key services
- Highlight specialists
- Showcase work
- Provide clear booking CTA

### 02 — Services

Browse available salon services.

### 03 — Service Detail

Detailed information about a service.

Potential information:

- Description
- Price
- Duration
- Eligible specialists
- Portfolio examples
- Booking CTA

### 04 — Specialists

Browse salon specialists.

### 05 — Specialist Profile

Potential information:

- Specialist information
- Skills/services
- Portfolio
- Reviews
- Availability
- Booking CTA

### 06 — Gallery / Portfolio

Browse salon work and visual examples.

---

# Booking Experience

The following are currently product steps.

They are NOT confirmed as individual routes.

### 07 — Select Service

Choose one or potentially multiple services.

### 08 — Select Specialist

Choose a specialist where applicable.

Potential future option:

"No preference / Any available specialist"

Not yet decided.

### 09 — Select Date & Time

Browse available dates and appointment times.

### 10 — Customer Details

Provide required booking/customer information.

### 11 — Review Booking

Review:

- Services
- Specialist
- Date
- Time
- Duration
- Price
- Relevant policies

before confirmation.

### 12 — Booking Confirmation

Display successful booking information and next actions.

---

# Authentication

### 13 — Login

Customer authentication.

### 14 — Sign Up

Customer account creation.

### 15 — Forgot Password

Account recovery.

Authentication strategy is not yet defined.

---

# Customer Account

### 16 — My Account

Customer account overview.

### 17 — My Appointments

View:

- Upcoming appointments
- Previous appointments
- Relevant appointment statuses

### 18 — Appointment Detail

View an individual booking.

Potential actions:

- Reschedule
- Cancel
- Rebook

Rules are not yet defined.

### 19 — Profile

Manage customer information and preferences.

### 20 — Favorites

Potential future feature.

Could include:

- Favorite services
- Favorite specialists

MVP inclusion undecided.

### 21 — Notifications

Potential customer notification center.

MVP inclusion undecided.

---

# Informational

### 22 — About

Salon information.

### 23 — Contact

Contact information and potentially map/location information.

### 24 — FAQ

Common questions, policies, and booking information.

---

# Salon Management Experience

## Authentication

### 25 — Admin Login

Authentication entry point for salon management.

Exact staff role model is not yet defined.

---

# Dashboard

### 26 — Dashboard

Operational overview.

Exact metrics should be determined later rather than invented during UI generation.

---

# Scheduling

### 27 — Calendar

Central salon appointment calendar.

Potential views:

- Day
- Week
- Staff

Exact views undecided.

### 28 — Appointments

Search/browse appointments.

### 29 — Appointment Detail

View and manage an individual appointment.

Potential capabilities:

- View customer
- View services
- View assigned specialist
- Change status
- Reschedule
- Cancel
- Add notes

Exact permissions and actions remain undefined.

---

# Customers

### 30 — Customers

Customer directory.

### 31 — Customer Detail

Potential information:

- Contact details
- Appointment history
- Preferences
- Notes
- No-show/cancellation history

Privacy and access rules will need later definition.

---

# Services

### 32 — Services

Manage salon service catalog.

### 33 — Service Detail / Edit

Potential fields:

- Name
- Description
- Price
- Duration
- Category
- Eligible specialists
- Booking availability

Exact data model remains undefined.

---

# Specialists

### 34 — Specialists

Manage salon specialists.

### 35 — Specialist Detail / Edit

Potential information:

- Profile
- Services
- Skills
- Portfolio
- Schedule
- Availability

### 36 — Specialist Schedule

Manage working hours and availability.

This may eventually be part of Specialist Detail rather than a dedicated route.

---

# Content

### 37 — Gallery

Manage salon portfolio/gallery.

### 38 — Reviews

View/manage customer reviews where appropriate.

Review moderation rules are not yet defined.

---

# Communication

### 39 — Notifications

Potential management area for customer communications and notification configuration.

Exact scope is undefined.

---

# Reporting

### 40 — Reports

Potential reporting/analytics experience.

MVP inclusion and metrics are not yet defined.

Do not invent vanity metrics solely to fill the dashboard.

---

# Configuration

### 41 — Settings

Potential areas:

- Salon information
- Business hours
- Booking rules
- Cancellation rules
- Notifications
- Payments
- Staff permissions

This will likely evolve into multiple settings screens or sections.

---

# Current Candidate Count

**41 candidate screens/experiences**

This number should NOT be treated as the final number of application pages.

---

# Major Open Decisions

Before converting this inventory into `page-manifest.md`, determine:

1. Is booking one route with multiple steps or multiple routes?
2. Can customers book multiple services together?
3. Can one booking involve multiple specialists?
4. Is specialist selection required?
5. Can customers select "any specialist"?
6. Which authentication screens actually need dedicated routes?
7. Which account experiences should be tabs rather than pages?
8. Which admin create/edit experiences should be routes vs modals/drawers?
9. Does Specialist Schedule need a dedicated page?
10. Should Settings be one experience or multiple routes?
11. Which candidate features belong in MVP?
12. What staff roles exist?
13. Which informational pages are actually necessary?
14. Does the product need payment/deposit screens?

---

# Next Step

Do not send this inventory to Base44 as the final page specification yet.

Continue:

Core User Journeys  
→ Capability Map  
→ Booking Model Decisions  
→ Route / Screen Decisions  
→ MVP Scope  
→ Final Page Manifest

Only after the Page Manifest is approved should the Base44 foundation prompt be generated.
