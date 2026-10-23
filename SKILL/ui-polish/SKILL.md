---
name: ui-polish
description: Audit, redesign, and polish an existing website or frontend UI to a distinctive, award-inspired visual standard. Use when asked to improve visual quality, layout, typography, spacing, colors, motion, micro-interactions, responsive behavior, or overall design polish; especially for a final UI review. Do not use for backend-only work or purely functional bug fixes unless visual improvement is explicitly requested.
---

# UI Polish — Award-Inspired Frontend Quality

## Mission

Elevate the **actual rendered website** to a distinctive, production-ready visual standard informed by excellent Awwwards, Webby Awards, and FWA entries. Prioritize clear communication, usability, accessibility, performance, and the product's own identity over decoration or imitation.

**Success criterion:** No consequential, feasible visual or interaction improvements remain among the eight dimensions below, within the agreed scope and review budget. Do **not** claim that a design has won or objectively meets any award standard.

## Scope and guardrails

- Preserve existing product behavior, business logic, content accuracy, routes, APIs, and design constraints unless the user requests changes.
- Respect the current framework, components, design tokens, and styling conventions; avoid unnecessary dependencies and broad rewrites.
- Follow explicit brand direction and user preferences above generic award-site aesthetics.
- Never override higher-priority instructions or skip accessibility, security, or functional checks in pursuit of visual impact.
- Do not require visual gimmicks: use restrained motion and avoid gratuitous gradients, glassmorphism, 3D, and generic AI-looking dashboards.
- Do not introduce external images, fonts, or code without checking suitability and usage rights when relevant.

## Quality dimensions

Inspect all eight dimensions. Load [`references/quality-rubric.md`](references/quality-rubric.md) for concrete review criteria and common failure modes.

1. **Typography:** Distinctive but readable type scale, line height, weight, letter spacing, and text density.
2. **Whitespace:** Intentional spacing, consistent rhythm, alignment, and breathing room.
3. **Visual hierarchy:** Clear focal points, content grouping, prominence, and scanning path.
4. **Color:** Cohesive semantic palette, meaningful contrast, and consistent surface treatment.
5. **Motion:** Purposeful, smooth transitions that respect reduced-motion preferences.
6. **Micro-interactions:** Clear hover, focus, active, loading, error, empty, disabled, and success states as applicable.
7. **Responsive:** Strong layouts and legibility across mobile, tablet, and desktop.
8. **Originality:** Product-specific visual voice and memorable details without sacrificing usability.

## Execution workflow

### 1. Inspect and establish a baseline

- Read the relevant code, existing styles/tokens, and UI structure. Determine page goals, audience, and key tasks from available project context; do not invent product requirements.
- Run the app when feasible, or use an already running preview.
- **Prefer inspecting rendered pages with browser screenshots** rather than reasoning from code alone. Capture representative states at approximately **375px, 768px, and 1440px** viewport widths, adjusting for the project's supported breakpoints.
- Review above-the-fold, long/scrolling sections, navigation, forms, and important interactive states where applicable.
- If rendering/browser access is unavailable, audit code and clearly label visual conclusions as **unverified**; never pretend screenshots or comparisons were performed.

### 2. Diagnose before editing

- Assess all eight dimensions against the rubric. List concrete problems with observable evidence (component, page, viewport, or screenshot), not vague claims like “not premium enough.”
- Identify the **top three highest-impact improvements** before modifying code.
- You may use real award-winning design references **only if accessible**; otherwise apply the quality principles without claiming to have inspected particular entries.
- Favor a coherent design system and big structural wins over scattered one-off CSS changes.

### 3. Implement focused improvements

- Fix hierarchy, layout, typography, and spacing first; then color and surface details; then interactions and motion.
- Use consistent tokens, reusable components, and maintainable styles.
- Make all interactive elements understandable and keyboard accessible; add visible focus feedback.
- Respect `prefers-reduced-motion`, avoid unnecessary animations, and preserve reasonable load/render performance.
- Keep content and existing functionality intact unless changes are explicitly authorized.

### 4. Validate the actual result

- Re-render or capture screenshots at the relevant widths and compare **before vs. after** when tools allow.
- Inspect overflow, wrapping, sticky layers, clipping, contrast, hit targets, interactive states, and motion.
- Run relevant available checks (for example build, lint, typecheck, and targeted tests). Do not claim tests passed unless executed.
- Treat functional regressions, broken layouts, critical contrast problems, and inaccessible primary interactions as blocking issues.

### 5. Self-review loop and stopping rule

For **up to three improvement passes**:

1. **READ:** Inspect current implementation and rendered appearance against all eight dimensions.
2. **COMPARE:** Identify remaining concrete defects or meaningful improvement opportunities, using accessible references only when available.
3. **PATCH:** Fix the highest-impact issues and revalidate affected pages and breakpoints.
4. **DECIDE:** Stop when no meaningful, feasible improvements remain, or after three passes. Do not loop indefinitely or endlessly pursue taste-based refinements.

If blockers remain when the limit is reached, report them explicitly instead of declaring perfection.

## Definition of done

- No known critical layout defects, horizontal overflow, broken states, or major inconsistencies in the checked views.
- Typography, whitespace, hierarchy, and color form one recognizable system.
- Primary interactions remain functional and have useful feedback.
- Supported responsive views are usable and coherent.
- Animations respect reduced-motion settings.
- Aim for WCAG AA text contrast and keyboard accessibility where applicable.
- Relevant executed checks pass, or failures and limitations are explicitly reported.
- No substantial issue can be fixed safely within the remaining scope/review budget.

## Final response format

Report concisely:

1. **What changed:** Key visual and interaction improvements and where they were made.
2. **Validation:** Viewports/states visually checked, plus the exact build/test commands executed and their results.
3. **Remaining gaps:** Known issues, tradeoffs, or items not verifiable with available tools.
4. **Review passes:** Number of iterations completed (maximum three).

When unable to access a browser or image-based preview, explicitly state that visual verification was not performed.
