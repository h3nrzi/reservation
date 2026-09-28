# Page Manifest

**Version:** 0.1

**Status:** Approved for Base44 foundation prototype

This manifest follows the core journeys and the first POC boundary. A route is a durable user destination; transient review steps, quote details, filters, and confirmations stay within a page.

## Layouts

- **Public:** Home and category guidance, with a clear request CTA.
- **Customer preview:** My Requests and Request Detail. No real account or authentication.
- **Provider preview:** Feed, Request Detail, and Jobs. A visible preview switch explains the simulated role.
- **Request creation:** Focused step layout; no competing marketing navigation while completing the form.

## Routes

| Route | Layout | POC purpose | Foundation state |
| --- | --- | --- | --- |
| `/` | Public | Explain request → quotes → assignment; start a request | Placeholder, first page to implement |
| `/categories` | Public | Browse trades and choose a request category | Placeholder |
| `/request/new` | Request creation | Structured problem intake and review | Placeholder, second page to implement |
| `/requests` | Customer preview | List sample requests and states | Placeholder |
| `/requests/:requestId` | Customer preview | Waiting, quote comparison, selection, assigned progress | Placeholder |
| `/pro/requests` | Provider preview | Suitable request feed with matching reason | Placeholder |
| `/pro/requests/:requestId` | Provider preview | Request context and quote submission | Placeholder |
| `/pro/jobs` | Provider preview | Assigned jobs and mock status changes | Placeholder |

## Within-page surfaces

- New Request steps: issue → location/urgency → review. Keep one route and preserve entered data between steps.
- Category selection on Home or Categories may prefill New Request.
- Quote details are an expandable card or drawer on Request Detail, not a route.
- Assignment confirmation is a dialog with a clear outcome.
- Filters and empty states stay in their list pages.
- Unknown request IDs show a designed not-found state within the relevant preview layout.

## Foundation stop

Base44 first creates all routes as identifiable placeholders, shared layouts, RTL direction, navigation, and design-token styling. It must stop before designing full pages. Then implement Home and New Request in separate page passes, reviewing each before proceeding.

## Explicitly absent

No login, checkout, chat, map, real provider directory, production admin, or booking calendar routes in this POC.
