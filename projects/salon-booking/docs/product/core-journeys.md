# Salon Booking Platform — Core User Journeys

**Version:** 0.1  
**Status:** Approved Discovery Baseline

## Purpose

Define the core end-to-end user journeys before finalizing routes, screens, or the Base44 page manifest.

---

# J1 — Discover & Book

Customer discovers the salon and completes an appointment booking.

Home / Discovery  
→ Explore Services / Portfolio / Specialists  
→ Select one or more Services  
→ Select a Specialist preference for each Service (`specific specialist` or `Any specialist`)  
→ Select Date / Availability  
→ System presents compatible booking options  
→ Enter Customer Details / Guest identity  
→ Review Booking  
→ Confirm Booking  
→ Receive Confirmation

## Approved Booking Decisions

- A booking may contain multiple services.
- Different services in the same booking may be assigned to different specialists.
- Specialist selection is optional; customers may choose `Any specialist`.
- Customers can inspect services, specialists, prices, and availability before authentication/customer details are required.
- Guest booking using a mobile number is supported for the initial product direction.
- The product should remain ready for future deposit/online payment without making payment mandatory in the first prototype.

## Important Product Implication

A multi-service booking is not necessarily a single start-time selection. The product may eventually need to construct a compatible booking plan across service durations, specialist capabilities, schedules, and existing appointments.

This document defines product behavior only. Scheduling algorithms and backend architecture are intentionally deferred.

---

# J2 — Manage Appointment

Customer accesses an existing appointment.

My Appointments  
→ Appointment Detail  
→ Review Booking Information  
→ Reschedule or Cancel when permitted  
→ Receive Updated Confirmation

Cancellation and rescheduling are governed by salon policies that remain to be defined.

Rebooking is a desirable follow-up capability.

---

# J3 — Salon Daily Operations

Salon management/staff operates the daily schedule.

Open Calendar  
→ Review Today's / Upcoming Appointments  
→ Open Appointment  
→ Review Customer + Services + Assigned Specialists  
→ Manage Appointment State

Candidate operational states include:

- Confirmed
- Arrived
- In Service
- Completed
- No-show
- Cancelled

The exact state model is not yet finalized.

---

# J4 — Manage Services & Specialists

Salon management configures the supply side of booking.

Manage Services  
→ Define Service Information / Price / Duration  
→ Define Which Specialists Can Perform Each Service  
→ Manage Specialists  
→ Define Working Schedules / Availability / Time Off

These definitions ultimately influence customer-visible availability.

---

# J5 — Customer Management

Salon staff manages customer context.

Find Customer  
→ Open Customer Detail  
→ Review Appointment History  
→ Review Relevant Preferences / Internal Notes where appropriate

Privacy, permissions, and the exact customer data model are deferred until the engineering/domain phase.

---

# Supporting / Future Journeys

The following are valuable but are not currently treated as core journeys for the first product scope:

- Waitlist
- Reviews
- Loyalty
- Promotions
- Favorites
- Gift cards
- Memberships
- Packages
- Referral
- Advanced reporting
- Personalized recommendations

---
