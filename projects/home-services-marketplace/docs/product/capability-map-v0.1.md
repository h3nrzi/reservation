# Capability Map and POC Boundary

**Version:** 0.1

## Capability domains

| Domain | POC capability | Later capability |
| --- | --- | --- |
| Request intake | Category, issue description, fictional area, urgency, optional sample images, review | Real uploads, precise address, fraud checks |
| Matching | Explain matching criteria through deterministic examples | Real ranking, geographic eligibility, capacity |
| Quotes | Two or more comparable mock offers, scoped amount and exclusions | Negotiation, quote expiration, on-site assessment |
| Assignment | Select one offer and update visible states | Provider acceptance, cancellation rules, disputes |
| Job lifecycle | Customer/provider status previews | GPS, dispatch, notifications, completion evidence |
| Trust | Fictional rating, completed-job count, verification label explained as mock | Identity verification, real reviews, guarantees |
| Operations | Read-only sample state for review if needed | Moderation, support, quality and fraud workflows |

## In the first Base44 prototype

- Public Home with a distinct request-first entry point and category guidance.
- New Request flow and review state.
- My Requests and Request Detail, including waiting, quote comparison, and assigned states.
- Provider Feed and a simple Quote Submission view.
- Deterministic sample records and explicit preview-role switch.
- Responsive, accessible Persian RTL UI.

## Outside the first prototype

- Real login, identity verification, provider onboarding, and production permissions.
- Backend, database, payments, actual image upload, geolocation, SMS, chat, or real-time updates.
- Dynamic pricing or automated matching/ranking engine.
- Multi-city operations, dispute resolution, and legal policies.

## Boundary rule

No prototype element may imply a real provider has received a request or that a real job has been booked. Simulated states should be labeled in a quiet but clear way. Do not add appointment-first flows that collapse this project into Salon Booking with a new theme.
