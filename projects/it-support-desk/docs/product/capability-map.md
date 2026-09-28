# IT Support Desk — Capability Map and POC Boundary

**Version:** 0.1

**Status:** Proposed frontend POC boundary

| Capability | First frontend POC | Later / unresolved |
| --- | --- | --- |
| Requester intake | Ticket form, required-field feedback, seeded categories | Attachments, email/chat intake |
| Requester tracking | Own list, ticket detail, conversation, reply, confirm/reopen | Real identity, notifications |
| Agent work | Shared queue, filters, assignment, priority, status, reply, resolution note | Routing automation, escalation rules |
| Manager oversight | Simple counts, at-risk/overdue examples, drill-down | Configurable SLA policy, analytics |
| Data and identity | Deterministic dummy data, role switch, local demo state/reset | Backend, persistence, authentication, authorization |

Keep the mock ticket shape consistent across requester, agent, and manager screens: identifier, subject, category, requester, assignee, priority, status, created/updated times, illustrative target time, conversation, and optional resolution note. This is a UI data contract for prototyping, not a database schema or production API.

The implementation boundary is **UI → an explicit ticket data/action interface → mock implementation** when the prototype moves to local engineering. Codex should evaluate the exported code before committing to that interface's final shape. Later, an API implementation can replace the mock behind the agreed contract, one vertical ticket journey at a time.
