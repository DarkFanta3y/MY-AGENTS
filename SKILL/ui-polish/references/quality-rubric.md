# UI Polish — Visual Quality Rubric

Use this rubric as a **diagnostic checklist**, not as a claim that a site qualifies for an award. Describe issues with concrete evidence. Favor clear, specific fixes.

| Dimension | Examine | Common failure signs |
| --- | --- | --- |
| Typography | Type scale, line length, hierarchy, font loading, weights, alignment, legibility | Same-size headings, tiny body text, wide lines, inconsistent weights |
| Whitespace | Spacing scale, padding, margins, grid alignment, negative space, mobile density | Arbitrary gaps, crowded cards, inconsistent section padding |
| Visual hierarchy | Most important action and content, scanning order, contrast, grouping | Everything competes for attention, unclear CTA, weak headings |
| Color | Brand identity, semantic states, surface layers, dark mode, contrast | Random accent colors, low-contrast labels, indistinguishable states |
| Motion | Easing, duration, continuity, perceived performance, reduced motion | Animation for its own sake, jank, excessive parallax, no reduced-motion handling |
| Micro-interactions | Hover, focus-visible, active, disabled, loading, error, success, empty states | Dead-feeling controls, no feedback, hidden focus, misleading click targets |
| Responsive | 375px/768px/1440px and project breakpoints, touch ergonomics, wrapping, navigation | Horizontal scroll, overlapping content, desktop-only interactions |
| Originality | Brand/product-specific choices, coherent motifs, content-led personality | Cookie-cutter dashboard, generic purple gradients, pasted visual trends |

## Severity and prioritization

- **Blocker:** Broken primary action, severe clipping/overflow, inaccessible critical control, serious regression.
- **High:** Weak hierarchy, illegible text, major responsive failure, confusing states.
- **Medium:** Noticeable inconsistency, awkward spacing, transitions, visual refinement with clear user benefit.
- **Low:** Purely subjective taste change or ornamental improvement without demonstrated user benefit.

Fix Blockers and High issues first. Prefer systemic fixes that improve several screens over individually tweaking many components.

## Practical checkpoints

### Typography and layout
- Check heading order and visual scale, body readability, navigation, and content density.
- Look at page-level rhythm, not just individual components.
- Avoid excessive font families and arbitrary pixel values where a design scale exists.

### Accessibility and motion
- Aim for WCAG AA contrast for text, with focus styles and keyboard access for functional controls.
- Honor `prefers-reduced-motion`; never make essential information depend only on animation.
- Check form errors and validation feedback, touch target sizes, and state distinctions beyond color alone.

### Screenshot comparison
- Compare matching routes, viewports, application states, and scroll positions.
- Inspect the hero or first screen, a dense-content region, and primary interaction states.
- If baseline screenshots are unavailable, say so; do not fabricate improvements.

### Exit decision
- Stop after no meaningful improvement remains **or** three rounds, whichever comes first.
- Never represent a subjective “award-tier” score as objectively verified.
- Document tool or environment constraints accurately.
