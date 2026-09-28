# Locale and Market Requirements

**Version:** 0.1

**Target:** Persian-first / Iran / RTL-native POC

## Approved presentation decisions

- All customer-facing copy and mock content are natural Persian. Technical filenames, route paths, IDs, and code symbols remain English.
- The document and page shells use RTL. Mixed-direction content such as phone examples, IDs, and Latin abbreviations must remain readable and isolated where needed.
- Use Vazirmatn or a comparable Persian UI font with reliable weight coverage and legible numerals.
- Display Persian digits in visible prices, counts, and sample dates. Keep underlying mock values numeric and deterministic.
- Display prices in **تومان**. A quote must distinguish estimated total from included work and any exclusions; do not claim fixed prices before a provider responds.
- Use Persian/Jalali labels for displayed sample dates. The POC may use fixed date strings; it does not need a production calendar or timezone engine.
- Use fictional neighborhoods/city labels and broad service areas. Never show a real residential address or exact location in sample data.
- Icons with directionality, progress steps, breadcrumbs, drawers, and carousels follow RTL reading order. Do not mirror neutral icons unnecessarily.
- Test narrow mobile and desktop layouts. Category and quote controls must remain usable by keyboard and touch.

## Deferred

- English localization and full i18n architecture.
- Real geocoding, map search, and local time conversions.
- SMS and phone verification.
- Legal terms, tax, and invoicing rules.

These choices are POC defaults and should be revisited before a real-market release.
