---
name: frontend-design
description: Guides the agent in building well-designed, accessible, and consistent frontend UIs using modern best practices.
---

# frontend-design

This skill helps the agent produce high-quality frontend interfaces with strong visual design, accessibility, and maintainability.

## When to use

Activate this skill when:
- Creating or modifying UI components, pages, or layouts
- Choosing color palettes, typography, or spacing
- Implementing responsive or adaptive designs
- Reviewing frontend code for design consistency
- Building design systems or component libraries

## Instructions

### Layout & Spacing
1. Use a consistent spacing scale (e.g. 4px base unit: 4, 8, 12, 16, 24, 32, 48, 64px).
2. Prefer CSS Grid for two-dimensional layouts and Flexbox for one-dimensional alignment.
3. Keep content width readable — max-width around 65–75ch for prose, wider for dashboards.
4. Use whitespace deliberately to create visual hierarchy; avoid cluttered UIs.

### Typography
1. Limit the font stack to 2 typefaces maximum (one for headings, one for body).
2. Maintain a clear type scale: base 16px, with ratios of 1.25 or 1.333 for headings.
3. Line-height for body text should be 1.5–1.6; tighter (1.2–1.3) for headings.
4. Never set text smaller than 14px for readability.

### Color
1. Define a design token system: primary, secondary, neutral, semantic (success, warning, error, info).
2. Ensure sufficient contrast: WCAG AA minimum 4.5:1 for body text, 3:1 for large text and UI components.
3. Do not rely on color alone to convey meaning — pair with icons or labels.
4. Support both light and dark modes using CSS custom properties (`--color-*`).

### Components
1. Build components to be self-contained with clear props/interfaces.
2. Prefer composability over monolithic components.
3. Use semantic HTML elements (`<button>`, `<nav>`, `<main>`, `<article>`, etc.) before reaching for `<div>`.
4. Keep component styling scoped — avoid global side effects.

### Accessibility (a11y)
1. All interactive elements must be keyboard-navigable and have visible focus styles.
2. Provide `alt` text for all meaningful images; use `alt=""` for decorative ones.
3. Use ARIA attributes only when semantic HTML is insufficient.
4. Ensure forms have associated `<label>` elements for every input.
5. Test with a screen reader and keyboard-only navigation before shipping.

### Responsiveness
1. Design mobile-first: start with the smallest viewport, then add breakpoints.
2. Use relative units (`rem`, `%`, `vw`, `vh`) over fixed `px` for fluid layouts.
3. Standard breakpoints: 480px (mobile), 768px (tablet), 1024px (desktop), 1280px (wide).
4. Images should use `srcset` or CSS `object-fit` to adapt to container size.

### Performance
1. Minimize layout shifts — set explicit `width`/`height` on images and media.
2. Prefer CSS animations over JavaScript animations for transforms and opacity.
3. Lazy-load below-the-fold images and non-critical components.
4. Avoid deeply nested selectors that increase specificity and hurt maintainability.

### Design Consistency
1. Follow the project's existing design system or component library conventions.
2. Use design tokens for all colors, spacing, and typography — avoid magic numbers.
3. When in doubt, align with the existing visual language before introducing new patterns.
