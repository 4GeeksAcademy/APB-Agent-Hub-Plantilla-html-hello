---
name: Autonomous Operations Console
colors:
  surface: '#0b1326'
  surface-dim: '#0b1326'
  surface-bright: '#31394d'
  surface-container-lowest: '#060e20'
  surface-container-low: '#131b2e'
  surface-container: '#171f33'
  surface-container-high: '#222a3d'
  surface-container-highest: '#2d3449'
  on-surface: '#dae2fd'
  on-surface-variant: '#c7c4d7'
  inverse-surface: '#dae2fd'
  inverse-on-surface: '#283044'
  outline: '#908fa0'
  outline-variant: '#464554'
  surface-tint: '#c0c1ff'
  primary: '#c0c1ff'
  on-primary: '#1000a9'
  primary-container: '#8083ff'
  on-primary-container: '#0d0096'
  inverse-primary: '#494bd6'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffb2b7'
  on-tertiary: '#67001b'
  tertiary-container: '#ff516a'
  on-tertiary-container: '#5b0017'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e1e0ff'
  primary-fixed-dim: '#c0c1ff'
  on-primary-fixed: '#07006c'
  on-primary-fixed-variant: '#2f2ebe'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffdadb'
  tertiary-fixed-dim: '#ffb2b7'
  on-tertiary-fixed: '#40000d'
  on-tertiary-fixed-variant: '#92002a'
  background: '#0b1326'
  on-background: '#dae2fd'
  surface-variant: '#2d3449'
typography:
  display-lg:
    fontFamily: Space Grotesk
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 52px
    letterSpacing: -0.03em
  display-lg-mobile:
    fontFamily: Space Grotesk
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.02em
  headline-xl:
    fontFamily: Space Grotesk
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 38px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Space Grotesk
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 30px
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Space Grotesk
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Space Grotesk
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.005em
  headline-sm:
    fontFamily: Space Grotesk
    fontSize: 15px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0em
  body-lg:
    fontFamily: Geist
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-md:
    fontFamily: Geist
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
    letterSpacing: -0.005em
  body-sm:
    fontFamily: Geist
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
    letterSpacing: 0em
  label-md:
    fontFamily: Geist
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.06em
  label-sm:
    fontFamily: Geist
    fontSize: 10px
    fontWeight: '600'
    lineHeight: 14px
    letterSpacing: 0.08em
  code-num:
    fontFamily: Geist
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
spacing:
  gutter: 1rem
  gutter-mobile: 0.75rem
  margin: 2rem
  margin-mobile: 1rem
  space-2xs: 0.125rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 0.75rem
  space-lg: 1.25rem
  space-xl: 1.75rem
  space-2xl: 2.5rem
---

## Brand & Style

The design system establishes a stark, uncompromising technical aesthetic for autonomous AI agent infrastructure. The visual language conveys high-throughput precision, cold computational efficiency, and operational control. The target audience comprises machine learning engineers, infrastructure directors, and automated enterprise system administrators who require dense, low-latency telemetry over decorative softness.

The emotional tone balances absolute mechanical reliability with industrial severity. Surfaces evoke terminal consoles, rack-mounted hardware instrumentation, and high-frequency trading terminals. The design movement merges **Technical Brutalism** with **Modern Data-Dense Functionalism**: razor-sharp boundaries, high-contrast operational status signaling, pitch-dark backdrops, and monoline structural grids. There are no ornamental rounded corners, no gratuitous skeuomorphic textures, and no decorative gradients. Form is strictly subordinate to operational observability.

## Colors

The color architecture is built for persistent low-light environments, prioritizing operational status triage and optical contrast over decorative balance.

- **Primary (`#6366F1`)**: Indigo beacon utilized exclusively for command actions, active pipeline selection, system focus states, and primary interaction triggers.
- **Secondary (`#10B981`)**: Emerald telemetry indicator signaling operational equilibrium, agent health, high compute availability, and active deployment states.
- **Tertiary (`#F43F5E`)**: High-saturation rose/crimson dedicated to agent failure alerts, runtime anomalies, throttling events, and critical circuit-breaker trips.
- **Neutral Palette (`#0F172A` Slate Base)**: The background surfaces descend from deep technical slate (`#020617` root background) to structural panel fills (`#0F172A` base layer, `#1E293B` elevated containers). Structural separation relies on precise slate borders (`#334155`).

### Status Badges & High-Contrast Signals
- **Active Agent**: Crisp `#10B981` typography over `#064E3B` / 20% alpha container, with a solid `#10B981` 1px border.
- **Inactive / Dormant Agent**: Muted `#94A3B8` typography over `#1E293B` container with `#475569` border.
- **Failing Agent**: Pure `#F43F5E` typography over `#881337` / 30% alpha container, reinforced by a pulsing `#F43F5E` perimeter key.

## Typography

Typography functions as an analytical instrument. `Space Grotesk` introduces deliberate geometric angularity and engineered authority to system titles, agent identifiers, and numerical metric headers. `Geist` provides neutral, hyper-legible rendering for dense log lines, tabular parameter feeds, and user configurations.

### Application Rules
- **Numerical Rigor**: All tabular agent runtime telemetry, latency numbers, and token balances rendered in `Geist` must enforce tabular numerals (`font-variant-numeric: tabular-nums`) to prevent horizontal jitter during real-time streaming updates.
- **Labels & Metatags**: Metric keys, telemetry markers, and status headers use uppercase `label-sm` or `label-md` with tracking stretched to `0.06em - 0.08em` for rapid legibility against dark slate surfaces.
- **Scale Compression**: On viewport widths below 768px, display titles contract via dedicated mobile scale tokens to prevent line wrapping in mission-critical parameter headers.

## Layout & Spacing

The layout is structured around an uncompromising 12-column modular grid with zero-deadband execution. Space is prioritized for information throughput, avoiding excessive whitespace in data monitoring views while maintaining strict rhythmic alignments.

### Grid Architecture
- **Desktop (1280px+)**: 12 columns, 1rem (`16px`) gutters, 2rem (`32px`) viewport margin. Layout sections occupy full operational widths (3-column KPI splits, 8/4 dashboard telemetry balance).
- **Tablet (768px - 1279px)**: 8 columns, 1rem gutters, 1.5rem margin. KPI cards wrap into 2x2 formations; tables gain horizontal scroll pinning on the primary agent identifier column.
- **Mobile (< 768px)**: 4 columns, 0.75rem (`12px`) gutters, 1rem (`16px`) canvas margin. Metrics collapse into single-column vertical stacks.

### Spacing Discipline
Internal container padding follows structural increments:
- Micro-indicators and tight table rows use `space-xs` and `space-sm`.
- Form inputs, metrics tiles, and control headers deploy `space-md` and `space-lg`.
- Major modular zones (e.g., global metrics band to real-time cluster view) separate via `space-xl` and `space-2xl`.

## Elevation & Depth

This design system rejects blurred ambient drop shadows and soft skeuomorphic layering. In a brutalist autonomous interface, physical depth is rendered strictly through tonal stratification and high-contrast structural borders.

### Depth Hierarchy
1. **Base Foundation (Level 0)**: `#020617` (Deep Obsidian Slate). The root canvas layer for the global viewport.
2. **Structural Panels (Level 1)**: `#0F172A` (Charcoal Slate). Background fill for data tables, KPI card bodies, sidebars, and control grids. Separated from Level 0 by a hairline `1px solid #1E293B` boundary.
3. **Interactive & Elevated Containers (Level 2)**: `#1E293B`. Surface for dropdown popovers, modal dialogs, flyout code inspectors, and agent configuration trays. Framed with high-definition `1px solid #334155`.
4. **Active Focus & Selection (Level 3)**: `#0F172A` paired with a sharp, offset border: `1px solid #6366F1` and an optional hard-offset boundary (`box-shadow: 2px 2px 0px 0px #6366F1`). Shadows are exclusively hard-edged directional offsets (zero blur radius).

## Shapes

The geometric philosophy is strictly uncurved (`roundedness: 0`). 

Every component—buttons, input fields, cards, tables, modal overlays, tooltips, and badges—features absolute 90-degree right angles (`border-radius: 0px`). This evokes industrial equipment terminals and precision computational interfaces. 

Visual separation is driven entirely through 1px border lines, surface brightness jumps, and sharp monoline framing. Status badges, buttons, and system chips remain rectilinear tiles.

## Components

### Buttons
- **Primary**: Solid `#6366F1` background, `#FFFFFF` text (`label-md`), 0px border radius, padding `0.5rem 1rem`. Hover state shifts fill to `#4F46E5`. Active state applies a hard inset frame `inset 0 0 0 1px #FFFFFF`.
- **Secondary / Ghost**: Background transparent, `#F8FAFC` text, `1px solid #334155` border. On hover, background shifts to `#1E293B` and border lightens to `#64748B`.
- **Destructive**: Background `#881337` / 30% alpha, `#F43F5E` text, `1px solid #F43F5E`. On hover, background becomes solid `#E11D48` with `#FFFFFF` text.

### High-Contrast Status Badges
Rectangular tags with micro-borders, 0px radius, tracked uppercase typography (`label-sm`).
- **Active**: Background `#022C22`, border `1px solid #10B981`, text `#34D399`. Prefixed with a static square 4px emerald indicator.
- **Inactive / Idle**: Background `#0F172A`, border `1px solid #475569`, text `#94A3B8`.
- **Failing**: Background `#450A0A`, border `1px solid #F43F5E`, text `#FDA4AF`. Accompanied by high-contrast telemetry alert text.

### KPI Cards
- Constructed with `#0F172A` surface, framed by `1px solid #1E293B`.
- Layout: Top rail displays the metric label (`label-sm`, `#64748B`) and status badge right-aligned. Midsection hosts the primary telemetry value in `Space Grotesk` (`headline-xl`, `#F8FAFC`). Bottom rail hosts tabular sparkline or delta readout (`+14.2% vs baseline` in `#10B981` or `#F43F5E`).
- Zero border radius; hover state updates border to `1px solid #334155`.

### Data Tables
- Header row utilizes `#020617` base fill, bordered on top and bottom by `1px solid #334155`. Header cells render `label-sm` in `#94A3B8`.
- Table body rows use alternating clean slate stripes (`#0F172A` and `#090D16`), separated by `1px solid #1E293B`.
- Interactive rows transition to background `#1E293B` on hover with a sharp 2px `#6366F1` vertical indicator running along the leftmost border.
- Agent telemetry columns (latency, memory, invocation count) strictly utilize `Geist` tabular figures.

### Input Fields & Controls
- **Inputs**: Flat `#020617` background, `1px solid #334155` border, `#F8FAFC` input text, 0px border radius. Focus state enforces `1px solid #6366F1` with an immediate sharp high-contrast highlight.
- **Dropdowns & Popovers**: Base fill `#0F172A`, outer boundary `1px solid #475569`. Menu items are rectangular blocks with padding `0.5rem 0.75rem`. Hovered options highlight in `#1E293B` with primary text rendered in `#6366F1`.
- **Checkboxes & Radios**: Strictly square (radios do not use circular styling; they are distinguished via internal square pip anchors). 14px outer dimension, `1px solid #475569`, filling with solid `#6366F1` on selection.

### Telemetry Logs & Terminal Drawers
- Specialized monospace log viewer embedded into bottom view drawers. Obsidian black background (`#000000`), bounded by a single `#1E293B` top divider. Log levels (`INFO`, `WARN`, `ERR`) styled via high-contrast `#6366F1`, `#F59E0B`, and `#F43F5E` micro-tags.