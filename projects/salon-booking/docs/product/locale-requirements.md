# Salon Booking Platform — Locale & Market Requirements

**Version:** 0.1  
**Status:** Approved Product Baseline  
**Primary Market:** Persian-speaking users / Iran-oriented salon experience

## Purpose

Define locale and market assumptions before regenerating the Base44 foundation. These requirements affect layout, typography, copy, dates, numbers, currency, dummy data, and directional UI behavior.

This is a Persian-first product. This document does not require full multi-language internationalization in the initial prototype.

---

# 1. Primary Language

Primary product language: **Persian (`fa`)**.

All user-facing prototype copy should be natural Persian, including:

- Navigation
- Page titles
- Buttons
- Form labels
- Placeholders
- Empty states
- Status labels
- Booking steps
- Admin navigation
- Dummy customer/service/specialist content

Engineering identifiers should remain English.

Examples:

- `ServiceCard`
- `BookingStep`
- `AppointmentStatus`
- `SpecialistProfile`

Do not translate component names, route implementation identifiers, variable names, or code architecture into Persian merely because the UI is Persian.

---

# 2. Writing Direction

The application must be **RTL-native**.

Use document/application direction appropriate for Persian rather than simulating RTL with text alignment alone.

RTL behavior must be considered for:

- Navigation
- Headers
- Admin sidebar
- Breadcrumbs
- Booking steppers
- Tabs
- Drawers
- Modals
- Pagination
- Forms
- Tables
- Calendar navigation
- Directional icons / chevrons / arrows
- Previous / next actions
- Responsive navigation

Directional UI should mirror where semantics require it.

Do not blindly mirror non-directional icons.

---

# 3. Typography

Primary Persian/UI typeface: **Vazirmatn**.

Vazirmatn should replace Inter as the primary functional typeface for Persian UI.

The previous English-only `Cormorant Garamond` display direction should not be used for Persian text.

For v0.1 Persian foundation, prefer a coherent Vazirmatn-based typography system rather than forcing an unrelated Latin editorial display font into Persian headings.

The premium/editorial character should instead come from:

- scale
- weight
- whitespace
- composition
- photography
- hierarchy

A separate Persian display typeface may be evaluated later if it provides clear value and appropriate licensing/availability.

Latin/numeric fallback should remain sensible where Latin content appears.

---

# 4. Numeral Policy

Default customer-facing UI numerals: **Persian digits**.

Example:

`۱۲۳۴۵۶۷۸۹۰`

Use Persian digits for normal presentation of:

- dates
- times
- prices
- counts
- appointment information
- durations

However, inputs and identifiers that benefit from normalized machine-readable entry must be handled deliberately.

Examples include:

- mobile phone numbers
- technical identifiers
- URLs
- internal IDs

The frontend should not assume that presentation formatting and stored/domain values are identical.

---

# 5. Calendar

Primary user-facing calendar system: **Jalali / Solar Hijri (Persian calendar)**.

Customer booking and customer-facing appointment dates should eventually use Jalali presentation.

Admin calendar/date experiences should also be designed for Persian/Jalali usage.

Important architectural constraint:

The UI calendar choice does not imply that future backend/domain timestamps must be stored as formatted Jalali strings.

Backend/domain date representation will be decided during engineering architecture. The frontend foundation should avoid hard-coding a storage strategy.

---

# 6. Date Formatting

User-facing dates should follow natural Persian conventions and use Persian month/day naming where appropriate.

Examples may resemble:

`شنبه ۱۵ آذر`

or where year is useful:

`۱۵ آذر ۱۴۰۵`

Exact compact/long format variants may be defined later by component context.

Do not expose US-style month/day ordering to users.

---

# 7. Time Formatting

Default time presentation: **24-hour time**.

Examples:

`۰۹:۳۰`

`۱۷:۰۰`

This is especially important for booking slots and salon/admin calendar experiences.

---

# 8. Currency

Primary customer-facing currency unit: **Toman (تومان)**.

Example presentation:

`۱٬۲۵۰٬۰۰۰ تومان`

Use readable thousands separators.

Do not scatter currency formatting logic across components. Future implementation should centralize locale-aware money formatting.

The eventual domain/API money representation will be decided during backend architecture.

---

# 9. Dummy Data

Prototype dummy data should feel native to the target market rather than translated from an English demo.

Use natural Persian examples for:

- Customer names
- Specialist names
- Service names
- Service descriptions
- Appointment labels
- FAQ content
- Salon information
- Status/contextual copy

Dummy data should be deterministic and reusable once detailed page implementation begins.

Foundation Pass v0.2 should still use only minimal dummy content required to verify routes/layouts.

---

# 10. Routes & URLs

Keep route paths and technical URL structure in English for v0.1.

Examples:

- `/services`
- `/specialists/:specialistId`
- `/book`
- `/appointments`
- `/admin/calendar`

Persian UI labels should not require Persian route slugs.

This keeps engineering conventions predictable and avoids unnecessary URL migration complexity during the prototype.

---

# 11. Customer Layout Direction

Customer/public experiences should be designed from RTL composition from the start.

Requirements include:

- RTL navigation order
- Correct heading/text alignment
- Correct placement of primary/secondary actions
- RTL-aware service/specialist metadata
- Correct directional icon behavior
- Persian typography spacing and line wrapping

Do not generate an LTR layout and merely right-align the text afterward.

---

# 12. Booking Experience Direction

The booking flow must be RTL-native.

Future booking steps remain conceptually:

1. انتخاب خدمات
2. انتخاب متخصص
3. تاریخ و زمان
4. اطلاعات مشتری
5. مرور رزرو
6. تأیید

The stepper/progress direction should visually make sense in RTL.

Date/time selection must be compatible with Persian/Jalali presentation.

---

# 13. Admin Layout Direction

The admin application must also be RTL-native.

Initial direction:

- Primary admin sidebar on the right on desktop
- RTL navigation hierarchy
- RTL-aware tables and filters
- Correct icon direction
- Persian labels and statuses
- 24-hour time
- Jalali-oriented calendar presentation

Data-heavy admin layouts should preserve efficiency; RTL must not be treated as an excuse to reduce information density or clarity.

---

# 14. Mixed-Direction Content

The UI may contain LTR fragments inside RTL contexts, such as:

- phone numbers
- URLs
- email addresses
- technical codes
- IDs

Implementation should handle bidi/mixed-direction content intentionally so these values remain readable and do not visually reorder surrounding Persian text incorrectly.

---

# 15. Design Direction Compatibility

The approved `Warm Luxury` direction remains valid.

Locale changes do not alter the core brand direction:

- Elegant
- Warm
- Calm
- Premium
- Trustworthy
- Modern

However, premium/editorial character must now be achieved with Persian-compatible typography and composition.

Do not preserve an English visual decision when it harms Persian readability or RTL usability.

---

# 16. Design Token Impact

The existing color, spacing, radius, shadow, control-height, and density principles remain valid unless later testing proves otherwise.

Typography must change for the Persian foundation:

Previous:

- Display → Cormorant Garamond
- Functional → Inter

Persian v0.1 direction:

- Primary Persian UI → Vazirmatn
- Persian headings/display → Vazirmatn with deliberate scale/weight initially

Directional layout values should prefer logical concepts such as start/end where the generated stack supports them, rather than unnecessary left/right assumptions.

---

# 17. Internationalization Scope

This product is currently **Persian-first**, not necessarily multilingual.

Foundation v0.2 should not add a language switcher or full translation-management system unless explicitly requested later.

The goal is to build the correct Persian product foundation, not to prematurely engineer a global localization platform.

At the same time, avoid unnecessary hard-coding patterns that would make future localization unusually difficult.

---

# 18. Accessibility

Existing accessibility requirements remain in force.

Additionally:

- Persian text must remain readable at all supported sizes.
- RTL focus/navigation order must remain logical.
- Directional icons must not communicate the wrong action after mirroring.
- Mixed LTR/RTL content must remain understandable.
- Persian digits must not reduce clarity in critical inputs.

---

# 19. Foundation v0.2 Acceptance Criteria

The regenerated Base44 foundation should demonstrate:

- Persian-first user-facing copy
- Native RTL application direction
- RTL Public Layout
- RTL Booking Layout
- RTL Customer Layout
- RTL Admin Auth Layout
- RTL Admin Layout
- Right-side desktop admin navigation
- Persian-compatible typography using Vazirmatn
- Persian numeral presentation in representative placeholders
- Jalali-aware date/calendar direction
- Toman-aware price presentation
- 24-hour time presentation
- Correct directional UI behavior
- English technical route paths preserved
- No unnecessary language switcher/full i18n platform

---
