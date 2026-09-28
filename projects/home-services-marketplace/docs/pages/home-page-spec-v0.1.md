# Home Page Specification

**Version:** 0.1

**Route:** `/`

**Goal:** A first-time visitor understands that they describe a home task, receive quotes, and choose a provider. The primary action starts a request.

## Required composition

1. Public header with brand, category link, customer request preview link, provider preview link, and clear `درخواست خدمت` action.
2. Compact hero with a concrete Persian promise, one primary CTA to `/request/new`, and secondary category exploration. No appointment/calendar language.
3. Three-step explanation: describe the issue → compare provider quotes → choose and follow the job. Make the simulated nature clear without dominating the page.
4. Six sample categories: plumbing, electrical, appliance repair, HVAC, cleaning, painting/handyman. Category action may prefill `/request/new`.
5. A believable example request with two differing quote summaries to demonstrate comparison. Use fictional provider data and label as a sample.
6. Trust explanation focused on scope clarity, comparable offers, and transparent provider signals. Do not claim real verification or guarantees.
7. Short FAQ addressing how pricing works, whether a provider is assigned automatically, and what happens after submission.
8. Final CTA and footer.

## Behavior

- All primary CTAs navigate to the New Request placeholder/page.
- Category selection passes a category context when practical; otherwise the selected category is visibly retained in mock state.
- Links to yet-unimplemented routes open their placeholders, not broken pages.
- Do not fabricate live counts, real ratings, or operational claims.

## Acceptance review

Within the first screen, a user should be able to distinguish this product from a booking website. Test narrow mobile and desktop for early CTA visibility, Persian readability, RTL navigation, and no horizontal overflow.
