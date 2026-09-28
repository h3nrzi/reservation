# Salon Booking Platform — Design Direction

**Version:** 0.1  
**Status:** Approved Design Baseline  
**Direction:** Warm Luxury

## Purpose

Define the visual and experiential intent that must guide Design Tokens and Base44 generation. This document intentionally sits above implementation values such as exact hex colors, Tailwind mappings, font sizes, and component-specific styling.

---

# Direction Summary

> A warm, editorial luxury salon experience for customers, paired with a calm and highly functional operational interface for salon staff.

The product should feel premium and feminine without relying on stereotypical pink-heavy styling, excessive gold, decorative clutter, or fake-luxury visual effects.

---

# Brand Personality

- Elegant
- Warm
- Calm
- Premium
- Trustworthy
- Modern

The experience should communicate professional beauty care and confidence rather than fashion gimmicks.

---

# Customer Experience Character

The customer-facing experience should be visual, aspirational, spacious, and easy to understand.

Priorities:

- Generous whitespace
- Strong visual hierarchy
- High-quality salon/portfolio photography
- Prominent services and specialists
- Clear booking calls to action
- Calm progression through booking
- Minimal visual noise

The interface should feel editorial where appropriate, while booking interactions remain obvious and functional.

---

# Admin Experience Character

The management surface should retain the same brand family without behaving like a marketing website.

Priorities:

- Functional clarity
- Faster scanning
- Higher information density than the customer surface
- Clear statuses and actions
- Efficient calendar and management workflows
- Reduced decorative imagery
- Consistent semantic colors and typography

The admin interface should feel calm and premium, but operational efficiency takes priority over visual drama.

---

# Color Direction

The palette should be based on warm neutrals with a restrained brand accent.

Direction:

- Ivory / Cream
- Warm White
- Sand / Stone
- Deep Espresso
- Muted Rose accent

Muted Rose should act as a controlled brand/accent color rather than turning the application predominantly pink.

Success, warning, destructive/error, and informational states should be semantic and remain distinguishable from the brand palette.

Exact color values are deferred to Design Tokens v0.1.

---

# Typography Direction

Customer-facing typography should combine an editorial premium character with highly readable modern UI typography.

Direction:

- Expressive/editorial treatment for selected high-level customer-facing headings
- Modern sans-serif for body text, controls, forms, navigation, and functional UI
- Admin surface should rely primarily on the functional sans-serif system
- Decorative typography must not reduce readability

Exact font families, weights, sizes, line heights, and responsive scale are deferred to Design Tokens.

---

# Shape & Surface Language

Direction:

- Medium radius
- Subtle borders
- Minimal shadows
- Selective card usage
- Generous whitespace on customer surfaces
- Clear grouping through spacing and hierarchy before adding containers

Avoid placing every piece of content inside a card.

Surfaces should feel refined and calm rather than layered with heavy shadows or effects.

---

# Imagery Direction

Photography is part of the brand experience, not decorative filler.

Priority subjects:

- Finished beauty results
- Detail shots
- Specialists
- Salon atmosphere
- Portfolio work

Imagery may play a major role in discovery, service, specialist, and gallery experiences.

As the customer moves deeper into the booking flow, imagery should become less dominant and task clarity should take priority.

Admin surfaces should use imagery only where operationally useful.

---

# Motion Direction

Motion should be subtle and purposeful.

Appropriate uses include:

- Selection feedback
- Booking-step transitions
- Drawer/modal transitions
- Small state changes
- Context-preserving UI transitions

Avoid animation whose primary purpose is decoration.

---

# Density Model

Different product surfaces intentionally use different density levels.

## Customer

**Comfortable / Spacious**

Optimize for discovery, confidence, visual presentation, and touch interaction.

## Booking

**Comfortable / Focused**

Reduce distractions and prioritize the current decision.

## Admin

**Compact / Efficient**

Optimize for repeated operational use, scanning, calendar management, and data actions.

Design Tokens and component variants should allow these density differences without creating unrelated design systems.

---

# Accessibility Principles

Premium styling must not depend on low contrast or ambiguous interactions.

Requirements:

- Readable muted text
- Clear focus states
- Appropriate touch/click target sizes
- Status meaning must not rely on color alone
- Controls should have recognizable interaction states
- Typography should remain readable across responsive sizes
- Decorative choices must not interfere with task completion

---

# Anti-Patterns

Base44 and later implementation should avoid:

- Excessive pink
- Excessive gold
- Glassmorphism
- Gradient-heavy UI
- Excessive shadows
- Card-everything layouts
- Giant rounded pills everywhere
- Decorative animation
- Generic SaaS dashboard styling
- Fake-luxury styling
- Low-contrast premium aesthetics
- Excessive visual decoration inside the booking flow

---

# Relationship to Design Tokens

This document defines intent.

`design-tokens-v0.1.md` should translate this direction into concrete reusable values and semantic tokens covering at minimum:

- Primitive colors
- Semantic colors
- Typography
- Spacing policy
- Radius
- Shadows
- Layout dimensions
- Responsive behavior / breakpoints policy
- Density guidance
- Focus and state styling

Design Tokens must be explainable by this Design Direction rather than chosen arbitrarily.

---

# Validation

During the Base44 foundation and page implementation phases, evaluate whether this direction:

- Produces consistent customer and admin experiences
- Reduces visual correction cycles
- Prevents generic AI-generated SaaS styling
- Keeps the salon identity premium without becoming stereotypical
- Gives enough constraint without preventing useful design exploration

Findings should be recorded in `workflow/workflow-feedback.md` where they affect the workflow itself.

---

# Next Step

Design Direction v0.1  
→ Design Tokens v0.1  
→ Base44 Foundation Prompt  
→ Foundation Review
