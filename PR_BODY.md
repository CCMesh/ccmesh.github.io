One-line summary:
Improve mobile navbar & hero spacing; standardize buttons/gradients; remove inline styles; minor accessibility fixes.

Summary:
- Compact mobile navbar and prevent the fixed header from overlapping hero titles.
- Add standardized button classes (`btn-meshcore`, `btn-meshtastic`, `btn-info`, `btn-compare`, `btn-gradient`, `btn-gradient-disabled`, `btn-disabled-alt`) in `includes/style.css`.
- Replace inline button/background styles across pages and consolidate gradients into `.btn-gradient`.
- Remove inline `padding-top` from hero sections so responsive CSS controls spacing.
- Accessibility tweaks: ensure images have `alt` and add `rel="noopener noreferrer"` to external links opened with `target="_blank"`.
- Captured desktop & mobile screenshots for visual verification.

Files changed:
- `includes/style.css`
- `index.html`
- `meshtastic-vs-meshcore.html`
- `mesh-in-emergency.html`
- `meshtastic.html`
- `meshcore.html`
- `lora.html`
- `config-meshcore.html`
- `config-meshtastic.html`

Testing (quick):
1. Serve locally:
   python -m http.server 8000
2. Visit http://localhost:8000 and verify:
   - Header/logo/title and H1 visibility on mobile and desktop
   - Button colors (Meshtastic green, MeshCore blue, compare teal)
   - Gradient button rendering and disabled states
   - No leftover inline hero `padding-top`
   - External `target="_blank"` links include `rel="noopener noreferrer"`

Reviewer checklist:
- Mobile header/hero titles render correctly in narrow viewports.
- Buttons render with correct colors and hover states.
- Spot-check hero sections and buttons for removed inline styles.
- Accessibility: `rel` on external links; images have `alt`.
- Visual regression: desktop layout and dropdown behavior.

Branch: ui/mobile-and-styles -> base: main
