# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a **12-panel animated SVG profile banner** (`/assets/profile-animation.svg`) showcasing data analytics, engineering, science, and ML expertise. The SVG uses **SMIL animations** (native SVG, no JavaScript) to cycle through rotating content panels in a **VS Code-themed interface**.

The banner is displayed in the GitHub profile README via:
```html
<img src="assets/profile-animation.svg" width="900" alt="Profile Animation"/>
```

## SVG Architecture

### Panel System (12 Panels, 30-Second Cycle)

Each of the 12 panels is a `<g>` (group) element with `<animate>` controlling opacity visibility. Panels are equally distributed: ~2.5 seconds per panel.

| # | Tab | Content | Time Window | keyTimes Pattern |
|---|-----|---------|-------------|------------------|
| 1 | query.sql | SQL SELECT, aggregates, results | 0–8.3% | `0;0.083;0.084;1` |
| 2 | analysis.py | Python pandas, numpy, correlation | 8.3–16.7% | `0;0.083;0.084;0.167;0.168;1` |
| 3 | dashboard.bi | Power BI KPI cards (revenue, users, conversion, AOV) | 16.7–25% | `0;0.167;0.168;0.250;0.251;1` |
| 4 | ml_model.py | Random Forest classifier training & metrics | 25–33.3% | `0;0.250;0.251;0.333;0.334;1` |
| 5 | schema.sql | Data warehouse schema (star schema, indexes) | 33.3–41.7% | `0;0.333;0.334;0.417;0.418;1` |
| 6 | stats.py | SciPy t-tests, correlation, confidence intervals | 41.7–50% | `0;0.417;0.418;0.500;0.501;1` |
| 7 | etl_pipeline.py | ETL pipeline monitor (Extract→Transform→Load progress) | 50–58.3% | `0;0.500;0.501;0.583;0.584;1` |
| 8 | bi_report.sql | BI metrics table (revenue, customers, churn, NPS) | 58.3–66.7% | `0;0.583;0.584;0.667;0.668;1` |
| 9 | viz.py | Data visualization (matplotlib/seaborn code + bar chart) | 66.7–75% | `0;0.667;0.668;0.750;0.751;1` |
| 10 | xgboost.py | XGBoost classifier & feature importance | 75–83.3% | `0;0.750;0.751;0.833;0.834;1` |
| 11 | optimize.sql | Query optimization (EXPLAIN ANALYZE) | 83.3–91.7% | `0;0.833;0.834;0.917;0.918;1` |
| 12 | summary.md | Executive summary (findings, recommendations) | 91.7–100% | `0;0.917;0.918;1` |

### SMIL Animation Mechanism

Each panel uses an `<animate>` element that is a **direct child of its `<g>` group**:

```xml
<g id="panelN" opacity="0">
  <!-- panel content: text, rects, etc. -->
  <animate attributeName="opacity" 
    values="0;0;1;1;0;0" 
    keyTimes="0;0.083;0.084;0.167;0.168;1" 
    dur="30s" 
    repeatCount="indefinite"/>
</g>
```

**Key constraints:**
- `keyTimes` must be monotonically increasing (0.083 < 0.084 < 0.167, etc.)
- `values` length must match `keyTimes` length
- All panels animate on the same 30-second cycle
- Panel 1 starts visible (opacity=1 at t=0); Panel 12 ends visible (opacity=1 at t=1)

### Static Chrome (Always Visible)

- **Top bar (y=0-35px):** Title "Data Analytics & Engineering Studio"
- **Tab bar (y=35-75px):** All 12 tab labels with animated opacity for active tab
- **Status bar (y=480-500px):** Footer info (blue background #007acc)

## Style & Appearance

### Color Palette (VS Code Dark Theme)

All colors use **inline `fill` attributes** (no CSS `<style>` blocks, as GitHub strips them):

| Element | Hex | RGB |
|---------|-----|-----|
| Background | `#1e1e1e` | Editor background |
| Text (default) | `#d4d4d4` | Normal text |
| Keywords | `#569cd6` | `SELECT`, `FROM`, `WHERE`, etc. |
| Functions | `#dcdcaa` | `SUM()`, `count()`, etc. |
| Strings | `#ce9178` | Quoted values |
| Comments | `#6a9955` | `--` and `#` comments |
| Numbers | `#b5cea8` | Numeric literals |
| Accent/Teal | `#4ec9b0` | Highlights & KPI values |
| UI (header) | `#252526` | Dark chrome |
| UI (status bar) | `#007acc` | VS Code blue |

### Typography

- **Code:** `font-family="Courier New,monospace"` at `font-size="13"`
- **UI labels:** `font-family="Segoe UI,Arial,sans-serif"` at 11–16px
- **KPI values:** Large bold sans-serif (18–22px) in accent color

### Layout Dimensions

- **Viewport:** 900×500px
- **Content area:** y=75 to y=480 (405px tall)
- **Code left margin:** x=65 (line numbers at x=44, right-aligned)
- **Typical line spacing:** 22px vertical

## Common Modification Tasks

### A. Change Animation Timing

**To slow down the cycle from 30s to 40s:**
1. Search for `dur="30s"` and replace with `dur="40s"`
2. Recalculate all `keyTimes` by multiplying by 40/30 = 1.333
   - Example: `0.083` becomes `0.111` (1.333 × 0.083)
   - Example: `0.167` becomes `0.223` (1.333 × 0.167)

### B. Add a New Panel

1. **In tab bar section (lines 12–83):**
   - Copy an existing tab `<g>` block
   - Update tab name text and width
   - Set initial `opacity="0"`
   - Adjust `keyTimes` for new panel's time window

2. **In panels section (lines 85+):**
   - Copy an entire panel `<g>` block
   - Update content (text, rects, shapes)
   - Recalculate all downstream panel `keyTimes` to fit new distribution

3. **Recalculate keyTimes for all panels:**
   - If adding 1 panel (now 13 total): each gets 30s ÷ 13 = ~2.31s
   - Panel N occupies: `((N-1)/13)` to `(N/13)` of the cycle

### C. Modify Content

- Edit `<text>` element content directly
- Adjust `x`, `y` coordinates if text length changes significantly
- Use `<tspan fill="#color">` for inline syntax highlighting
- Example:
  ```xml
  <text x="65" y="115" font-family="Courier New,monospace" font-size="13">
    <tspan fill="#569cd6">SELECT</tspan>
    <tspan fill="#d4d4d4"> customer_id FROM orders</tspan>
  </text>
  ```

### D. Update Colors

- Search-replace hex codes directly (e.g., `#569cd6` → `#4a8fff`)
- Maintain contrast ratios for readability (WCAG AA minimum 4.5:1 for text)
- Remember: inline `fill="..."` attributes, not CSS

### E. Resize the Banner

- Change `viewBox="0 0 900 500"` to new dimensions
- Scale all x/y/width/height coordinates proportionally
- Update README reference: `width="900"` to match viewBox width

### F. Add Animation Effects

- SMIL `<animate>` is limited to single attributes (opacity, etc.)
- For multi-attribute animation, use multiple `<animate>` elements on same group
- Cannot animate fill colors in time-sync with opacity (would require separate animations)

## Important Constraints

1. **No CSS:** GitHub strips `<style>` blocks from SVGs. All colors must use inline `fill="..."` attributes on individual elements.

2. **No JavaScript:** SMIL animations are the only animation mechanism. No click handlers or DOM manipulation.

3. **Panel Overlap:** All 12 panels are stacked at the same x/y position. Opacity animates to show/hide them; only one is visible at a time.

4. **Monotonic keyTimes:** Values like `0;0.083;0.084;0.167;0.168;1` must always increase. The tiny gaps (0.083 → 0.084, 0.167 → 0.168) create instant snap transitions between panels.

5. **Infinite Loop:** Animation loops forever. Ensure Panel 12 ends with opacity=1 at t=1 so it wraps smoothly to Panel 1 at t=0.

## File Organization

```
/home/user/anotther/
├── README.md                           # Profile with SVG reference
├── CLAUDE.md                            # This file
└── assets/
    └── profile-animation.svg            # Main 30-second animated banner
```

## Testing & Verification

**To verify animation renders correctly:**
1. Open `assets/profile-animation.svg` in a browser (Chrome, Firefox, Safari, Edge all support SMIL)
2. Observe all 12 panels cycling smoothly every ~2.5 seconds
3. Confirm colors match VS Code dark theme
4. Check that no panels overlap or flicker

**To test in GitHub README:**
1. Commit changes locally and push to your branch
2. View PR preview on GitHub
3. Note: GitHub's SVG rendering is static in most README contexts; animations may not play in preview but will work when hosted elsewhere

## Performance Notes

- **File size:** ~58KB (compressed, reasonable for a single banner)
- **GPU acceleration:** SMIL animations are GPU-accelerated in modern browsers
- **No external dependencies:** Pure SVG, no fonts, images, or libraries loaded
- **Compatibility:** SMIL is deprecated in favor of CSS/Web Animations but widely supported; works in all major browsers

## Git History Context

Recent commits focused on fixing:
- **CSS stripping issue:** GitHub removes `<style>` blocks → migrated to inline `fill` attributes
- **SMIL syntax errors:** Invalid element wrappers (`<opacity_animate1>`) → direct `<animate>` children of `<g>`
- **README path:** Updated from root `profile-animation.svg` to `assets/profile-animation.svg`
