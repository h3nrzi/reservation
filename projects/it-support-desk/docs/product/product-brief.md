# IT Support Desk — Product Brief

**Version:** 0.1

**Status:** Initial discovery proposal

## Problem and product hypothesis

In a small company, IT requests scattered across chat and email are hard to prioritize, assign, and close visibly. A shared ticket workspace should let an employee submit and follow a request, an agent move it through a clear workflow, and a manager see which requests need attention before an SLA target is missed.

The first POC tests whether that end-to-end experience is understandable. It is a frontend demonstration, not a working service desk.

## Portfolio distinction

Salon Booking centers on choosing services, specialists, and available appointment times. IT Support Desk centers on an already reported problem and its changing ownership, priority, conversation, deadline, and resolution. It is also distinct from the other catalog options: it does not match external providers, track vehicles or properties, coordinate moving or deliveries, dispatch field technicians, plan events, manage creative proposals, or run renovation phases. Those may produce requests, but the core here is an internal support ticket and its SLA.

## Roles

- **Employee / requester:** Submit an issue, see own tickets and updates, add a reply, and close or reopen a resolved ticket in the prototype.
- **Support agent:** Review the team queue, inspect context, set priority, assign an owner, reply, and resolve a ticket.
- **IT manager:** See queue health and SLA risk, filter for overdue or unassigned work, and open the same ticket detail for follow-up. Manager permissions beyond this view are deferred.

For the prototype, a visible role switch may simulate these perspectives. It is not authentication or authorization.

## Initial frontend POC boundary

Use one fictional company, a small fixed set of employees and agents, and deterministic tickets with varied statuses and SLA states. The interface should demonstrate:

1. Employee submits a ticket with subject, category, description, and optional urgency; the new ticket appears in their list.
2. Agent triages an unassigned ticket, sets priority and owner, posts a reply, and moves it through **New → In progress → Resolved**.
3. Employee sees the status and conversation, then closes the resolved ticket or reopens it. **Closed** is the final display state for this demo.
4. Manager scans counts and a simple at-risk/overdue list, then opens a ticket for context.

Demo interactions may update in-memory state; predictable reset behavior should restore the seeded scenario. Mock timestamps and SLA targets should be internally consistent. Show empty, validation, and error/blocked-action states where they matter to the journey, without pretending that messages, notifications, or data persist remotely.

## Out of scope for this POC

Real login and permissions; backend, database, API, persistence across sessions, email/chat ingestion, notifications, attachments, asset inventory, knowledge base, automation, complex SLA policies, reporting beyond the simple manager overview, and integrations. No production SLA enforcement is implied by a visual due-time label.

## Open decisions before Base44

- Locale, language, writing direction, typography, date/time format, and sample-content conventions need explicit agreement before routes and visual design are approved.
- Choose whether priority is agent-set only, and define the few visible priority and SLA examples. These are demonstration rules, not a final policy.

The next artifacts are a brief locale decision, approved page manifest, and design direction. Base44 should then create only route/layout placeholders and stop for review. Page implementation follows incrementally. After prototype approval: export to localhost, assess generated architecture with Codex, define domain and interface contracts, build backend slices, and replace mock data through those contracts. Do not predesign database tables at this stage.
