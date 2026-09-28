# Core User Journeys

**Version:** 0.1

## J1 — Customer requests help

Home → choose a category or describe a problem → New Request → select category, describe issue, choose fictional area and urgency, optionally add sample photos → review summary → submit mock request → request detail with `Awaiting quotes` state.

The flow asks for enough context to quote, without forcing the customer to choose a provider or booking slot first. The review step must make the request editable before submission.

## J2 — Customer compares and assigns

My Requests → request detail → inspect quote cards → compare estimate, scope, earliest start, provider rating and completed jobs → open quote detail → choose one → confirm assignment → request becomes `Assigned`; other quotes show `Not selected`.

If no quotes are present, show a clear waiting state and what the customer can do next. A withdrawn/expired quote must not be selectable.

## J3 — Provider responds

Provider request feed → open suitable request → review issue, area, urgency, sample photos and matching reason → submit quote with estimated amount, included work, exclusions, and earliest availability → see `Quote sent`. If already assigned or outside service area, disable quote action with explanation.

## J4 — Assigned work progresses

Provider jobs → assigned job → mark `On the way`, `In progress`, then `Completed` in the mock preview. Customer request detail reflects the same status. No real dispatch, GPS, payment, or notifications occur.

## Preview and failure states

- Use an explicit customer/provider preview switch rather than pretending to have real accounts.
- Validation: missing category, too-short description, or missing area must show actionable inline errors.
- Duplicate submission and no-match states need a visible, non-deceptive outcome.
- Mock persistence may be limited to the current session; the UI must say so when relevant.
