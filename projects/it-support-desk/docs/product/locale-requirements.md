# IT Support Desk — Locale Requirements

**Version:** 0.1

**Status:** Persian and RTL confirmed for the first POC; formatting defaults below are prototype assumptions

## Language and direction

Use natural Persian for all visible navigation, labels, statuses, validation, empty states, and fictional ticket content. Build the interface RTL-native, including the requester form, operations sidebar, filters, tables, dialogs, and directional icons. Keep route paths and engineering identifiers in English. No language switcher or full multilingual system is needed in the first POC.

Use Vazirmatn as the primary UI typeface. Treat email addresses, URLs, ticket IDs, and technical strings as LTR fragments within RTL text so their characters remain in order. Copy and paste must preserve those values.

## Prototype display conventions

For reproducible dummy data, assume **fa-IR**, **Asia/Tehran**, the **Jalali calendar** for displayed dates, **24-hour time**, and Persian digits in ordinary UI text. These are presentation choices for the initial prototype and can be revised if the target company differs. Show an absolute target time alongside relative SLA wording where useful; do not let a relative label depend on the viewer's real clock in the deterministic demo.

Keep ticket IDs, email addresses, URLs, and other machine-readable values in Latin characters and LTR order. Let inputs accept sensible Persian or Latin numerals where relevant, but do not require number entry in a ticket description. Store no assumptions about future backend timestamp format in this document.

## Direction and accessibility checks

- Place the primary operations navigation on the right at desktop widths; keep reading and keyboard focus order logical.
- Mirror directional chevrons and previous/next controls where their meaning changes in RTL. Do not mirror non-directional symbols.
- Keep mixed Persian/Latin ticket subjects and IDs readable in queues and detail views.
- Show status and SLA state through text and shape/icon cues as well as color.
- Use natural Persian sample names, categories, and messages; avoid real personal or company data.
