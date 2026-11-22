---
name: Autonomous Operations Console
colors:
  surface: '#faf8ff'
  surface-dim: '#d2d9f4'
  surface-bright: '#faf8ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f3ff'
  surface-container: '#eaedff'
  surface-container-high: '#e2e7ff'
  surface-container-highest: '#dae2fd'
  on-surface: '#131b2e'
  on-surface-variant: '#464555'
  inverse-surface: '#283044'
  inverse-on-surface: '#eef0ff'
  outline: '#777587'
  outline-variant: '#c7c4d8'
  surface-tint: '#4d44e3'
  primary: '#3525cd'
  on-primary: '#ffffff'
  primary-container: '#4f46e5'
  on-primary-container: '#dad7ff'
  inverse-primary: '#c3c0ff'
  secondary: '#0051d5'
  on-secondary: '#ffffff'
  secondary-container: '#316bf3'
  on-secondary-container: '#fefcff'
  tertiary: '#005338'
  on-tertiary: '#ffffff'
  tertiary-container: '#006e4c'
  on-tertiary-container: '#7df1bd'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e2dfff'
  primary-fixed-dim: '#c3c0ff'
  on-primary-fixed: '#0f0069'
  on-primary-fixed-variant: '#3323cc'
  secondary-fixed: '#dbe1ff'
  secondary-fixed-dim: '#b4c5ff'
  on-secondary-fixed: '#00174b'
  on-secondary-fixed-variant: '#003ea8'
  tertiary-fixed: '#85f8c4'
  tertiary-fixed-dim: '#68dba9'
  on-tertiary-fixed: '#002114'
  on-tertiary-fixed-variant: '#005137'
  background: '#faf8ff'
  on-background: '#131b2e'
  surface-variant: '#dae2fd'
typography:
  headline-xl:
    fontFamily: Space Grotesk
    fontSize: 36px
    fontWeight: '600'
    lineHeight: 44px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Space Grotesk
    fontSize: 28px
    fontWeight: '600'
    lineHeight: 36px
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Space Grotesk
    fontSize: 28px
    fontWeight: '600'
    lineHeight: 36px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Space Grotesk
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Space Grotesk
    fontSize: 16px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: 0em
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 18px
  label-lg:
    fontFamily: Space Grotesk
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-md:
    fontFamily: Space Grotesk
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: Space Grotesk
    fontSize: 10px
    fontWeight: '600'
    lineHeight: 14px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 1rem
  margin: 1.5rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 0.75rem
  space-lg: 1rem
  space-xl: 1.5rem
---

## Brand & Style
The design system establishes a high-precision, utilitarian operational environment for mission-critical telemetry, fleet automation, and cloud orchestration. Designed for systems engineers, technical operators, and site reliability teams, the interface delivers maximum visual clarity under demanding conditions.

The aesthetic fuses modern enterprise technical discipline with tactical minimalism. It avoids superfluous decorative treatments, leaning instead into rigorous structural alignment, razor-sharp density, and explicit status hierarchy. High-contrast typography pairs with focused electric indigo accents to highlight interactive states and system alerts without creating cognitive overload during continuous monitoring.

## Colors
The palette leverages a calibrated light-mode hierarchy engineered for daylight operations, command centers, and prolonged screen exposure:

- **Surface Layers:** Primary canvas rests on pure white (`#ffffff`), secondary workspace modules and structural frames utilize Slate-50 (`#f8fafc`), while inactive backgrounds, inset panels, and table headers adopt Slate-100 (`#f1f5f9`).
- **Dividers & Structural Rules:** Boundaries are strictly delineated by crisp, low-tolerance borders using Slate-200 (`#e2e8f0`) for internal cell division and Slate-300 (`#cbd5e1`) for primary pane perimeters.
- **Brand & Action Accents:** Electric Indigo (`#4f46e5`) serves as the primary focal driver for primary commands, focused elements, and active tracking indicators. Cobalt Blue (`#2563eb`) supports secondary interactions, deep analytics links, and operational controls.
- **Operational Status:** System telemetry is codified with zero ambiguity: Emerald Green (`#059669`) signals operational health and nominal states; Amber (`#d97706`) indicates queued, degraded, or staged actions; Rose (`#dc2626`) commands immediate visual priority for alerts, anomalies, and failures.
- **Text & Contrast:** Slate-900 (`#0f172a`) anchors critical telemetry, metric readouts, and primary headers at optimal contrast ratios. Slate-600 (`#475569`) provides balance for contextual metadata, inline units, and secondary labels.

## Typography
Typography reflects the contrast between technical instrumentation and high-density readability. 

- **Space Grotesk** serves as the display and metric face. Its structural, geometric letterforms convey technological exactitude across KPIs, console module headers, numeric counters, and system breadcrumbs.
- **Inter** handles narrative execution, data grids, logs, and system documentation. It remains neutral, highly legible at small sizes, and frictionless during dense data consumption.
- Numerical data tables and high-frequency real-time metrics should leverage tabular figures (`tnum`) to eliminate layout jitter during active data polling.

## Layout & Spacing
The layout follows a modular multi-pane workbench paradigm designed for maximum screen utilization across desktop and workstation form factors:

- **Grid Architecture:** Desktop displays operate on a 12-column variable fluid grid framed by persistent structural toolbars (64px fixed left navigation and 48px global status header). Gutters remain locked at `1rem` (16px) to maximize operational density without visual collision.
- **Adaptive Breakpoints:**
  - **Desktop (1440px+):** Full multi-pane telemetry layout (3 to 4 side-by-side data containers, full visibility data tables, dynamic graph inspectors).
  - **Tablet / Laptop (1024px – 1439px):** Collapsible secondary inspector sidebars; grid consolidates into 6-8 active columns with preserved `1rem` gutters.
  - **Mobile (< 1024px):** Single-column stacked stream. Margin shifts to `1rem`, tables convert into dense card lists, and sticky bottom sheets manage operational controls.
- **Spacing Discipline:** Spacing units prioritize structural rhythm over excessive breathing room. Internal component padding favors compact bounds (`space-sm` for table cells and chips, `space-md` for standard form controls and utility cards).

## Elevation & Depth
Depth in the console is established through flat surface stratification and crisp containment boundaries rather than heavy drop shadows:

- **Tonal Stratification:** Visual priority is defined by container layering. Base workspace canvas uses `#ffffff`. Inset monitors, side rails, and card containers sit on `#f8fafc`. Header strips, grouped cell rows, and input troughs drop to `#f1f5f9`.
- **Low-Contrast Outlines:** Every card, data grid, and interactive quadrant is bounded by a 1px solid border (`#e2e8f0` for interior groupings; `#cbd5e1` for outer card borders). 
- **Ambient Focus Elevation:** Floating elements (dropdown menus, command palettes, and floating contextual flyouts) employ ultra-subtle ambient shadows (`0 4px 12px rgba(15, 23, 42, 0.06), 0 1px 2px rgba(15, 23, 42, 0.04)`) overlaid against a solid white container with a 1px `#cbd5e1` stroke, maintaining a crisp, architectural finish.

## Shapes
The shape language adheres to Level 1 Soft geometry. All interactive components, panels, input fields, and tags utilize subtle `0.25rem` (4px) corner radii. Structural cards and modal dialogs extend to `0.5rem` (8px). 

This restrained corner rounding avoids decorative softness, signaling an uncompromising, technical workstation where every pixel is aligned to a rigorous Cartesian grid. Fully rounded pills are strictly reserved for operational status badges to instantly differentiate state indicators from actionable buttons.

## Components

### Buttons
- **Primary Action:** Solid Electric Indigo (`#4f46e5`) background, `#ffffff` text, 4px corner radius, font: Space Grotesk 14px medium. Hover: `#4338ca`. Active: `#3730a3`. Focus: 2px offset ring in `#4f46e5`.
- **Secondary Action:** Pure white (`#ffffff`) background with a 1px solid Slate-300 (`#cbd5e1`) border, Slate-900 (`#0f172a`) text. Hover: `#f8fafc` background with `#94a3b8` border.
- **Destructive Action:** Solid White background with a 1px solid Rose-300 (`#fca5a5`) border, Rose-700 (`#b91c1c`) text. Hover: Rose-50 (`#fff1f2`). Active: Rose-100 (`#ffe4e6`).

### Status Badges & Chips
- **Geometry:** Height 20px, pill-shaped radius (9999px), Space Grotesk 10px uppercase with `0.05em` letter spacing. Padding: 2px 8px.
- **Active / Nominal:** Emerald-50 background (`#ecfdf5`), 1px solid Emerald-200 (`#a7f3d0`), Emerald-700 text (`#047857`). Includes a 6px pulsing emerald dot indicator.
- **Staged / Warning:** Amber-50 background (`#fffbeb`), 1px solid Amber-200 (`#fde68a`), Amber-800 text (`#92400e`).
- **Error / Offline:** Rose-50 background (`#fff1f2`), 1px solid Rose-200 (`#fecdd3`), Rose-700 text (`#b91c1c`).

### Inputs & Form Fields
- **Container:** Height 36px, background `#ffffff`, 1px solid Slate-300 (`#cbd5e1`), 4px border radius. Padding: 0 12px. Font: Inter 14px Slate-900.
- **States:** Hover border shifts to Slate-400 (`#94a3b8`). Focused state activates a crisp 1px border in Electric Indigo (`#4f46e5`) with a 2px outer aura (`rgba(79, 70, 229, 0.15)`). Placeholder rendered in Slate-400.

### Checkboxes & Radios
- **Checkboxes:** 16x16px, 4px border radius. Unchecked: `#ffffff` with 1px Slate-300 border. Checked: `#4f46e5` background with white check icon.
- **Radio Buttons:** 16x16px circular boundary. Checked: White fill with a 6px inner circle in `#4f46e5`.

### Data Cards & Modules
- **Structure:** Background `#ffffff`, bounded by a 1px solid Slate-200 (`#e2e8f0`) frame, 8px border radius.
- **Header Strip:** Height 44px, background `#f8fafc`, separated by a bottom 1px border in Slate-200. Features Space Grotesk 14px bold title, metadata slot, and trailing mini-action buttons.
- **Body Area:** Direct padding of `1rem` (16px), optimized for telemetry graphs, data stream lists, and metric summaries.

### Telemetry KPI Widgets
- **Display:** Stacked layout with a small-caps category label (Space Grotesk 11px uppercase in Slate-500) over a large numerical readout (Space Grotesk 28px semi-bold in Slate-900 with tabular figures). Inline trend badge indicates positive or negative velocity with directional micro-arrows.