# New Request Page Specification

**Version:** 0.1

**Route:** `/request/new`

**Goal:** Help a customer describe a household problem well enough for a provider to quote, then review and submit a simulated request.

## Steps within one route

1. **Issue:** choose a category, short title, detailed description, optional example photo selection. Explain what details help the provider. Do not upload files.
2. **Area and timing:** choose a fictional city area, urgency (`عادی`, `این هفته`, `فوری`), and preferred broad time window. This is preference context, not a booked slot.
3. **Review:** show all entered data, clear edit links, and a reminder that price is set by provider quotes. Submit a mock request.

## Required behavior

- Preserve input when navigating between steps and when returning to edit.
- Use persistent labels and inline errors for missing category, title, useful description, and area. Errors should name the field and how to fix it.
- Show a clear post-submit confirmation with a fictional request ID and `در انتظار پیشنهادها` state, plus a route to `/requests/:requestId` or `/requests`.
- Distinguish the mock preview from a real request. Never imply a provider was contacted.
- A category selected on Home should appear as the initial selection when passed in navigation.
- Prevent an accidental second submission within the same visible flow.
- Do not ask for real name, phone number, exact address, or payment data in this prototype.

## Layout and copy

- Focused form layout with visible progress, concise step instructions, readable Persian examples, and an obvious Back action.
- A short side/help panel on desktop may explain the quote process; on mobile place help below the current step.
- One dominant action per step. Use neutral styling for secondary navigation.

## Acceptance review

Walk through both valid and invalid inputs at mobile and desktop widths. Confirm RTL step order, keyboard focus, persistent state, no real upload, and honest confirmation copy. Record non-blocking issues in the UI backlog.
