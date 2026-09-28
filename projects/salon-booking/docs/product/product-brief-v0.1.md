# Salon Booking Platform — Product Brief

**Version:** 0.1  
**Status:** Discovery Draft

## Product Type

Service-based website and booking platform for a women's beauty salon.

---

# Problem

Traditional appointment management for beauty salons can become difficult when bookings depend on phone calls, in-person scheduling, messaging, manual calendars, staff memory, and repeated communication about available times.

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
- Configure booking behavior
- Monitor salon activity

Exact roles and permissions have not yet been defined.

---

# Product Surfaces

The product has two major experiences:

## Customer Experience

Public discovery, booking, and customer appointment management.

## Salon Management System

Internal operational experience for managing appointments, customers, services, specialists, schedules, and salon configuration.

These experiences may share the same application/repository but should be treated as distinct product surfaces.

---

# Approved Booking Model v0.1

The following product decisions are approved for the current discovery baseline:

1. A customer can select multiple services in one booking.
2. Different services within the booking may be handled by different specialists.
3. Specialist selection is optional. Customers may choose a specific specialist or `Any specialist`.
4. Booking direction is: Services → Specialist preference → Date / compatible availability → Customer details → Review → Confirm.
5. Guest booking is supported using a mobile number; creating an account is not mandatory for the initial direction.
6. The product should remain ready for future deposit/online payment, but payment is not mandatory in the initial prototype/MVP.
7. Customers should be able to cancel or reschedule appointments subject to salon policies.
8. Waitlist is a future capability and is outside the initial MVP.

---

# Primary Customer Journey

Current approved direction:

Home / Discovery  
→ Explore Services / Portfolio / Specialists  
→ Select one or more Services  
→ Choose Specialist preference per Service (`specific` or `Any`)  
→ Choose Date / View Compatible Availability  
→ Enter Customer Details  
→ Review Booking  
→ Confirm Booking  
→ Booking Confirmation  
→ My Appointments

Customers should be able to explore services, specialists, prices, and availability before customer details/authentication become necessary.

See `core-journeys-v0.1.md` for the complete journey baseline.

---

# Post-Booking Journey

Booking should not be treated as the end of the customer lifecycle.

Current direction:

Booking  
→ Reminder  
→ Appointment  
→ Future Review / Rebook opportunities

---

# Product Inspiration

The product should not clone an existing platform.

## Fresha

Inspiration for overall salon booking product model, appointments, services, staff/resources, and client management.

## Booksy

Inspiration for customer booking flow, service/specialist discovery, availability, rebooking, and customer-facing experience.

## Vagaro

Inspiration for salon operations, calendar management, staff/provider management, and administrative workflows.

These references are for product research, not visual copying.

---

# Current MVP Direction

The initial product scope focuses on proving the end-to-end booking and salon-management loop.

Core MVP direction includes:

- Salon/service discovery
- Services
- Specialists
- Portfolio/gallery
- Availability
- Multi-service booking
- Guest customer flow
- Booking confirmation
- My Appointments
- Cancel / Reschedule
- Reminder capability
- Management calendar
- Appointment management
- Customer management
- Service management
- Specialist management
- Specialist schedules
- Basic salon/booking settings

Explicitly outside the initial MVP:

- Mandatory online payment/deposit
- Waitlist
- Reviews
- Favorites
- Loyalty
- Memberships
- Packages
- Gift cards
- Referral
- Promotions
- Advanced reporting
- Personalized recommendations

See `capability-map-v0.1.md` for the detailed capability boundary.

---

# Important Open Booking Questions

The product direction is clearer, but several policy/scheduling details remain intentionally unresolved.

## Duration

Services may have different durations. Some may have fixed durations while others may eventually vary.

## Specialist Capabilities

Not every specialist is expected to perform every service. Service-to-specialist eligibility must be represented in the product.

## Specialist Availability

Specialists have individual working schedules and availability.

## Salon Resources

Some services may eventually require resources in addition to a specialist, such as a chair, room, equipment, or device.

Resource-aware scheduling is not yet confirmed as an MVP requirement.

## Booking Policies

Still to be defined:

- Minimum advance booking time
- Maximum advance booking window
- Cancellation deadline
- Rescheduling rules
- No-show handling
- Late arrival rules
- Buffer time between appointments

---

# Current Product Hypothesis

At a conceptual level, appointment availability may eventually depend on:

Service  
+ Specialist Capability  
+ Duration  
+ Specialist Schedule  
+ Existing Appointments  
+ Salon Rules  
+ Possibly Resource  
= Compatible Booking Options

This is a product hypothesis only. Backend architecture and scheduling algorithms should not be designed yet.

---

# Current Phase

**Product Discovery — MVP boundary established**

Completed discovery artifacts:

- Product Brief v0.1
- Core User Journeys v0.1
- Capability Map / MVP Boundary v0.1
- Candidate Page Inventory v0.1

Next expected activity:

Revise Page Inventory using MVP Boundary  
→ Route / Screen Decisions  
→ Final Page Manifest  
→ Design Tokens  
→ Base44 Foundation
