# IT Support Desk — Core Journeys

**Version:** 0.1

**Status:** Proposed for POC discovery

## J1 — Employee requests help

My tickets → New ticket → Enter subject, category, description, optional urgency → Review required fields → Submit → Ticket detail. The new ticket is **New**, with its requester and submission time visible. If required fields are missing, show an inline error and keep the draft.

## J2 — Agent triages and resolves

Team queue → Filter unassigned/new → Ticket detail → Read request and conversation → Set priority and assign owner → Move to **In progress** → Reply → Resolve with a short resolution note. The queue and detail should agree after every demo action. A ticket cannot be resolved without a resolution note in the prototype.

## J3 — Employee follows up

My tickets → Ticket detail → Read status, owner, and replies → Add a reply. When resolved, the employee can mark it **Closed** or reopen with a reason. A reopened ticket returns to the agent queue as **In progress**; the earlier conversation remains visible. Exact production state and notification rules are deferred.

## J4 — Manager spots risk

Overview → Review counts for new, in progress, unassigned, at risk, and overdue → Open an at-risk or overdue ticket → Inspect owner, priority, target time, and recent activity. The POC uses fixed illustrative SLA targets and a fixed current time so the same scenario is reproducible. This is a display of risk, not an SLA engine.

## Common alternate states

Lists need a useful empty state. The role switch changes visible perspective and scope of lists; it does not grant security. Failed submission or invalid state changes need clear local feedback. Refresh may reset demo changes to the original seed data.
