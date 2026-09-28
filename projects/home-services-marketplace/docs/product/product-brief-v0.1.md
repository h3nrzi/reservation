# Home Services Marketplace — Product Brief

**Version:** 0.1

**Status:** POC direction

## Problem and promise

When a household task needs a specialist, a customer often has to describe the issue repeatedly, guess which trade is appropriate, compare vague prices, and coordinate through scattered messages. Providers need enough context to decide whether a job fits and to quote it consistently.

The product gives the customer one structured request, a short set of comparable offers, and a clear choice of who will do the work. The first POC demonstrates the marketplace loop rather than real scheduling or payment.

## Users

- **Customer:** describes the problem, reviews quotes, assigns one provider, and follows job status.
- **Provider:** sees suitable requests, reviews details, submits a scoped quote, and updates assigned work.
- **Operations reviewer:** sees request and quote states and can resolve a visibly flagged issue in a later phase. The POC uses a read-only preview, not an operational admin system.

## Distinct portfolio value

Salon Booking is service catalog → availability → appointment. This project is customer need → provider matching → competing quotes → assignment. A service category helps describe the problem; it is not the primary transaction.

## POC success criteria

With deterministic mock data, a reviewer can:

1. Understand how to describe a home issue and submit a request.
2. See which information providers receive and why a provider is considered suitable.
3. Compare at least two offers by total estimate, included work, earliest availability, and provider trust signals.
4. Choose one offer and observe the resulting job state in customer and provider previews.
5. Tell clearly what is simulated and what is not live.

## Initial constraints

- Persian-first, RTL-native experience for the Iranian market; detailed presentation rules are in the locale document.
- Single-city fictional sample data; no exact addresses, real phone numbers, or real provider identities in the prototype.
- Frontend-only Base44 prototype with deterministic mock state. No real matching, notifications, payment, messaging, or authentication.
- Price is a **provider estimate** until a quote is chosen, never a guaranteed catalog price.
- A request may receive multiple quotes; only one can be assigned.

## Open decisions after prototype validation

- Verification requirements for providers and trust signals.
- Quote expiration, cancellation, and re-quote policies.
- Whether on-site assessment is a separate quote type.
- Location precision and privacy boundaries.
- Payment, disputes, and service guarantee model.

Do not design backend or database tables from these unresolved questions.
