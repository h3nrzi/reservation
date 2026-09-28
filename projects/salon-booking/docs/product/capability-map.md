# Salon Booking Platform — Capability Map

**Version:** 0.1  
**Status:** Approved Discovery Baseline

## Purpose

Map the capabilities required to support the approved core journeys before deciding final pages/routes.

---

# Capability Domains

## Service Catalog

- Service categories
- Service discovery
- Service details
- Pricing
- Duration
- Multi-service selection

## Specialists

- Specialist profiles
- Skills / eligible services
- Specialist-specific schedules
- Availability
- `Any specialist` preference

## Availability

- Salon working hours
- Specialist working hours
- Existing appointment conflicts
- Time off / closures
- Compatible slot discovery
- Support for multi-service booking requirements

Exact scheduling algorithms are deferred.

## Booking

- Multi-service booking
- Per-service specialist preference/assignment
- Date and availability selection
- Booking review
- Confirmation
- Guest booking

## Customer

- Guest identity via mobile number
- Customer information
- Appointment history
- Customer preferences / notes where appropriate

## Appointment

- Appointment detail
- Appointment status
- Cancel
- Reschedule
- Rebook direction

## Calendar

- Salon calendar
- Daily/weekly operational visibility
- Specialist schedule visibility

## Salon Operations

- Appointment management
- Arrival / service progress
- Completion
- Cancellation
- No-show handling

Exact operational state model remains to be finalized.

## Content

- Salon information
- Gallery / portfolio
- FAQ / useful booking information

## Communication

- Booking confirmation
- Appointment reminders
- Updated confirmation after reschedule/cancellation

Real notification infrastructure is not part of the Base44 prototype; the UX/state should still be represented where relevant.

## Policies

Future/required booking configuration may include:

- Cancellation window
- Rescheduling window
- Minimum booking lead time
- Maximum advance booking window
- Buffer time
- Late arrival behavior
- No-show rules

Exact values and rules are not yet defined.

## Payment

The product architecture should remain compatible with:

- Deposit requirements
- Online payment

Payment is not mandatory in the initial prototype/MVP boundary.

## Access

- Customer identity / guest booking
- Salon management authentication
- Future staff role/permission model

Detailed authorization is deferred.

## Reviews

Post-appointment review capability is desirable but outside the initial MVP boundary.

## Waitlist

Customers may eventually request notification when a desired unavailable time becomes available.

Outside initial MVP.

## Growth

Future candidates:

- Favorites
- Loyalty
- Offers
- Referral
- Gift cards
- Memberships
- Packages
- Personalized recommendations

## Reporting

Advanced operational/business reporting is outside initial MVP.

---

# MVP Boundary v0.1

The initial product scope should focus on the booking loop and the minimum salon operations required to support it.

## In MVP

- Public salon discovery
- Services
- Specialists
- Portfolio/gallery
- Availability discovery
- Multi-service booking
- Per-service specialist preference
- `Any specialist`
- Guest customer flow
- Booking review and confirmation
- My Appointments
- Appointment detail
- Cancel / Reschedule
- Appointment reminders as a product capability
- Admin/management calendar
- Appointment management
- Customer management
- Service management
- Specialist management
- Specialist schedules / availability
- Basic salon/booking settings

## Outside Initial MVP / Backlog

- Mandatory online payment / deposit
- Waitlist
- Reviews
- Favorites
- Loyalty
- Memberships
- Service packages
- Gift cards
- Referral program
- Promotions
- Advanced reporting
- Personalized recommendations

---

# Boundary Principles

1. A capability being outside MVP does not mean the architecture must make it impossible later.
2. Future capabilities should not create pages or UI complexity in the Base44 prototype unless needed for the MVP experience.
3. The MVP should prove the end-to-end booking and salon-management loop before growth features are added.
4. Reminder UX belongs to the MVP product model, while real notification delivery infrastructure is deferred to engineering.
5. Payment readiness should influence future contracts/architecture, but payment UI should not dominate the first prototype.

---
