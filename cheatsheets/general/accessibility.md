---
id: cheatsheet-accessibility-interview-001
title: Accessibility interview cheatsheet
type: cheatsheet
domain: frontend
category: accessibility
audience: interview candidates
tags: [accessibility, inclusive-design]
status: review
---

# Start Native

Use semantic HTML controls before recreating behavior. A robust custom control needs accessible name, role, state, keyboard behavior, focus, visible focus, and understandable feedback.

# Quick Checks

- Logical heading and landmark structure
- Labels/instructions/errors associated with controls
- Complete keyboard journey and sensible focus movement
- Text/controls not identified by color alone; sufficient contrast
- Zoom/reflow, text spacing, reduced motion, and target size considered
- Dynamic status announced appropriately without excessive interruption

# ARIA Rules of Thumb

- Prefer native semantics.
- ARIA changes exposed semantics, not interaction behavior.
- Do not add conflicting/redundant roles.
- Test name/role/value/state in the accessibility tree.

# Testing

Combine review of requirements, keyboard testing, automated tools, and representative assistive-technology testing. Automation finds only a subset of barriers.

# Related Content

- [Accessible control question](../../questions/frontend/browser/accessibility.md)
