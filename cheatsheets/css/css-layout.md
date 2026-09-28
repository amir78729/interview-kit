---
id: cheatsheet-css-layout-001
title: CSS layout cheatsheet
type: cheatsheet
domain: frontend
category: css
audience: interview candidates
tags: [css, layout]
status: review
---

# Choose a Layout Model

| Need | Good starting point |
| --- | --- |
| One-dimensional distribution | Flexbox |
| Rows and columns together | Grid |
| Normal document content | Flow/block/inline layout |
| Overlay anchored to a box | Positioned layout |

# Flexbox

- Main/cross axes depend on direction and writing mode.
- `flex-basis` starts sizing; grow/shrink distribute free space.
- Auto minimum size can prevent truncation: investigate `min-width: 0`.

# Grid

- Explicit tracks are declared; placement can create implicit tracks.
- `fr` receives leftover space after constraints.
- `minmax()` plus `auto-fit`/`auto-fill` can reduce brittle breakpoints.

# Positioning and Stack

- Absolute boxes leave normal flow; relative boxes retain their space.
- Sticky needs an inset, scroll range, and compatible overflow ancestors.
- `z-index` compares within stacking contexts; find context boundaries before raising values.

# Responsive Reminders

Use intrinsic sizing and content-driven breakpoints; preserve zoom, source order, long/localized text, reduced motion, and touch targets.
