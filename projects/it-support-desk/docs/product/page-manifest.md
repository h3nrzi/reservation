# IT Support Desk — Proposed Page Manifest

**Version:** 0.1

**Status:** Candidate route plan; locale and design direction not yet approved

| Route | Surface | Purpose |
| --- | --- | --- |
| `/my/tickets` | Requester | Own tickets, status and search/filter; entry to new ticket |
| `/my/tickets/new` | Requester | Focused ticket submission form |
| `/tickets/:ticketId` | Shared detail | Ticket context, conversation, activity, and role-appropriate actions |
| `/agent/queue` | Agent | Team work queue, unassigned/priority/SLA filters |
| `/manager/overview` | Manager | Queue counts and at-risk/overdue tickets with drill-down |

The ticket detail is one route shared across perspectives; visible actions depend on the demo role. Triage, assignment, priority, reply, resolve, close, and reopen can use inline controls or dialogs within that detail. They are not separate pages. A role switch belongs in the application shell; there is no login page in the first POC.

**Layout families:** Requester workspace and internal operations workspace may share primitives while keeping navigation appropriate to each role. The first Base44 foundation pass should create only these routes, shells, and placeholders, then stop for review. Approve this manifest after locale and journey decisions; do not treat it as evidence that a Base44 pass has happened.
