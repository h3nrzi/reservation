# Salon Booking Platform — Product Brief

**Version:** 0.1  
**Status:** Discovery Draft

## Product Type

Service-based website and booking platform for a women's beauty salon.

---

# Problem

Traditional appointment management for beauty salons can become difficult when bookings depend on:

- Phone calls
- In-person scheduling
- Messaging
- Manual calendars
- Staff memory
- Repeated communication about available times

The product should make discovering, booking, and managing salon appointments significantly easier for both customers and salon staff.

---

# Primary Goal

Create an excellent online appointment-booking experience for salon customers while giving the salon a centralized system for managing appointments and related operations.

The product should eventually extend beyond basic appointment scheduling with additional features that improve customer experience, retention, and salon operations.

---

# Primary Users

## Customer

Primarily women looking for beauty and salon services.

Customer goals include:

- Discover available services
- Understand pricing and duration
- View specialists
- View previous work / portfolios
- Find available appointment times
- Book without calling the salon
- Manage existing appointments
- Receive reminders
- Return and book again easily

## Salon Management / Staff

People responsible for operating the salon.

Their goals may include:

- Manage appointments
- View the salon calendar
- Manage customers
- Manage services
- Manage specialists
- Manage staff schedules and availability
- Manage portfolio content
- Manage reviews
- Configure booking behavior
- Monitor salon activity

Exact roles and permissions have not yet been defined.

---

# Product Surfaces

The product currently appears to require two major experiences:

## Customer Experience

Public discovery and appointment booking.

## Salon Management System

Internal operational experience for managing appointments and salon resources.

These experiences may share the same application/repository but should be treated as distinct product surfaces.

---

# Primary Customer Journey

Initial happy-path hypothesis:

Home  
→ Explore Services  
→ View Service  
→ Choose Service  
→ Choose Specialist  
→ Choose Date  
→ View Available Times  
→ Choose Time  
→ Authenticate / Enter Customer Details  
→ Review Booking  
→ Deposit / Payment if Required  
→ Booking Confirmation  
→ My Appointments

Important UX hypothesis:

Customers should preferably be able to explore services, specialists, prices, and availability before being forced to create an account.

Authentication should happen closer to booking confirmation unless later product requirements indicate otherwise.

---

# Post-Booking Journey

Booking should not be treated as the end of the customer lifecycle.

Potential lifecycle:

Booking  
→ Reminder  
→ Appointment  
→ Review  
→ Rebook

Future customer-retention capabilities may extend this journey.

---

# Product Inspiration

The product should not clone an existing platform.

Current reference products:

## Fresha

Primary inspiration for:

- Overall salon booking product model
- Appointment ecosystem
- Services
- Staff/resources
- Client management

## Booksy

Primary inspiration for:

- Customer booking flow
- Service discovery
- Specialist discovery
- Availability
- Rebooking
- Customer-facing booking experience

## Vagaro

Primary inspiration for:

- Salon operations
- Calendar management
- Staff/provider management
- Administrative workflows

These references are for product research, not visual copying.

---

# Potential Future Capabilities

Not all of these belong in the MVP.

Candidate capabilities include:

- Smart waitlist
- Loyalty points
- Gift cards
- Promo codes
- Service packages
- Memberships
- Favorite specialists
- Favorite services
- Book again
- Before/after portfolio
- Customer preferences
- Customer history
- Service notes
- Birthday offers
- Referral program
- Automated reminders
- Cancellation rules
- Deposits
- Reviews
- Special offers
- Personalized recommendations
- Notifications

These remain backlog candidates until prioritized.

---

# Important Booking Questions

The booking model is not yet fully defined.

Questions requiring discovery include:

## Multiple Services

Can a customer book multiple services in one booking?

Example:

Hair Color  
+  
Manicure

## Multiple Specialists

If multiple services are booked, can different specialists perform each service?

Example:

Hair Color → Specialist A  
Manicure → Specialist B

## Duration

Services may have different durations.

Some may have fixed durations while others may vary.

The exact scheduling rules are not yet defined.

## Specialist Capabilities

Can every specialist perform every service?

Likely not.

The relationship between services and specialists must be defined.

## Specialist Availability

Specialists will likely have individual working schedules and availability.

Exact rules remain undefined.

## Salon Resources

Some services may require resources in addition to a specialist.

Examples could include:

- Chair
- Room
- Equipment
- Device

Whether resource-aware scheduling is required for the MVP remains undecided.

## Booking Rules

Still undefined:

- Minimum advance booking time
- Maximum advance booking window
- Cancellation deadline
- Rescheduling rules
- Deposits
- No-show handling
- Late arrival rules
- Buffer time between appointments

---

# Current Product Hypothesis

At a conceptual level, appointment availability may eventually depend on:

Service  
+ Specialist  
+ Duration  
+ Schedule  
+ Existing Appointments  
+ Possibly Resource  
= Available Time Slots

This is a product hypothesis only.

Backend architecture and scheduling algorithms should not be designed yet.

---

# MVP Status

MVP scope has not yet been finalized.

Current discovery should first establish:

1. Core user journeys
2. Core capabilities
3. Booking model
4. Customer vs management responsibilities
5. Route/screen structure

Only then should the final MVP page manifest be created.

---

# Current Phase

**Product Discovery**

Next expected activity:

Core User Journeys  
→ Capability Map  
→ Booking Decisions  
→ Page/Screen Decisions  
→ Page Manifest
