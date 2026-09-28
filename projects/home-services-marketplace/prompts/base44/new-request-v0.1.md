# Base44 Page Prompt — New Request

**Pass:** Implement `/request/new` only

Using the existing foundation and Home page, implement **only `/request/new`**. Preserve the Persian-first RTL UI, focused Request Creation layout, semantic tokens, Practical Trust visual language, and existing routes. This is a problem-intake flow for provider quotes, **not** an appointment booking form. After this page is complete, **STOP**.

## Flow within one route

1. **Issue:** choose one of the six established categories, enter a short title and useful description, and optionally select a simulated example photo. Explain which details help a provider prepare a quote. Do not perform a real upload.
2. **Area and timing:** choose a fictional area and urgency (`عادی`, `این هفته`, `فوری`), plus a broad preferred time window. No calendar or reserved slot.
3. **Review:** show the complete request with edit links and explain that providers will estimate price. The final action submits **mock data only**.

## Functional requirements

- Preserve entered values when moving back and forth between steps.
- If Home navigation passes a category, preselect it while allowing edits.
- Validate missing category, short/empty title, insufficient description, and missing area with useful inline Persian errors.
- Show a clear confirmation with a fictional request ID and `در انتظار پیشنهادها` state. Provide navigation to the customer request placeholder/detail; do not imply any real provider was contacted.
- Prevent repeated submissions in the same visible flow.
- Do not ask for real name, phone number, exact address, payment details, or account creation.
- Keep all sample data deterministic. If persistence is only temporary, say so in the preview UI.

## Layout and quality

Use a readable RTL progress indicator, one dominant action per step, obvious Back and Edit controls, persistent labels, accessible focus/error states, and comfortable mobile field spacing. A brief help panel may explain the quote process but must not distract from completing the request. Test valid and invalid paths at narrow mobile and desktop widths.

## Completion report

Report the working flow and any unresolved issue. Do not implement My Requests, provider pages, backend, or other routes. **STOP**.
