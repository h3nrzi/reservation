# Design Direction — Practical Trust

**Version:** 0.1

**Status:** Direction for the Base44 prototype

## Intent

The product should feel capable, clear, and calm when a home problem is stressful. It must help a user understand what happens after submitting a request and compare offers without sales pressure.

This visual personality differs from Salon Booking's Warm Luxury: it is a practical marketplace with strong information hierarchy, restrained color, transparent process cues, and evidence-led provider cards.

## Visual principles

1. **Request first:** The main CTA is `درخواست خدمت`, not a calendar or appointment action. Show the three-stage marketplace process near the top.
2. **Structured clarity:** Use concise labels, short guidance, and progressive disclosure. Forms should show what information improves a quote.
3. **Comparable offers:** Price, included scope, earliest availability, and trust signals occupy consistent positions across quote cards.
4. **Grounded trust:** Use believable service photography/illustrations only when useful. Avoid generic smiling stock workers as proof of verification.
5. **Operational precision:** Status labels and progress states should read like a reliable product, not decorative badges.

## Palette and typography direction

- Deep slate/navy for text and primary surfaces.
- Warm off-white background and clean white cards for readable density.
- Teal for primary action and progress; amber only for time-sensitive attention.
- Avoid Salon Booking's muted-rose/luxury palette.
- Vazirmatn with a clear Persian type scale. Titles concise; supporting copy comfortable on mobile.

## Layout direction

- RTL native at every breakpoint.
- Desktop: useful max-width, purposeful asymmetry between explanation and task form, no oversized empty hero.
- Mobile: primary request action visible early, form labels and help text readable, comparison cards stack without horizontal overflow.
- Use real information density where it helps decisions. Do not fill pages with decorative cards or empty metrics.

## Images and icons

- Prefer categories represented by simple coherent icons and at most a few authentic-feeling home-context images.
- Any image must have a stable fallback and descriptive alt text when informative.
- Directional arrows must follow RTL navigation; neutral tools and house icons remain unchanged.

## Review criteria

Check whether a first-time visitor understands the request/quote model, whether each major action is visually unambiguous, and whether the UI looks like a marketplace rather than a salon booking clone. Record non-blocking issues in the UI backlog.
