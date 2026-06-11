---
name: Forensic Provenance System
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#45464d'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#76777d'
  outline-variant: '#c6c6cd'
  surface-tint: '#565e74'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#131b2e'
  on-primary-container: '#7c839b'
  inverse-primary: '#bec6e0'
  secondary: '#006c49'
  on-secondary: '#ffffff'
  secondary-container: '#6cf8bb'
  on-secondary-container: '#00714d'
  tertiary: '#735c00'
  on-tertiary: '#ffffff'
  tertiary-container: '#cba72f'
  on-tertiary-container: '#4e3d00'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dae2fd'
  primary-fixed-dim: '#bec6e0'
  on-primary-fixed: '#131b2e'
  on-primary-fixed-variant: '#3f465c'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffe088'
  tertiary-fixed-dim: '#e9c349'
  on-tertiary-fixed: '#241a00'
  on-tertiary-fixed-variant: '#574500'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  display-lg:
    fontFamily: Geist
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Geist
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
  headline-lg-mobile:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  headline-md:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.05em
  label-xs:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '500'
    lineHeight: 12px
    letterSpacing: 0.1em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  gutter: 24px
  margin: 32px
  container-max: 1280px
---

## Brand & Style

The design system is engineered for **VerisArt**, a forensic-grade platform for artwork certification. The brand personality is rooted in **Authority, Precision, and Absolute Trust**. It balances the sterile, clinical nature of a forensic laboratory with the high-end, prestigious world of fine art.

The visual style is **Modern Corporate / Minimalist**, prioritizing clarity and information density. It utilizes expansive whitespace, rigorous grid alignment, and subtle technical accents to evoke a sense of high security. The interface should feel like a digital vault: impenetrable yet accessible to the right hands.

## Colors

The palette is designed to signal institutional credibility and technological validation.

- **Primary (Deep Navy):** Used for typography, navigation sidebars, and primary action buttons to establish authority.
- **Secondary (Tech Green):** Reserved for validation states, "Verified" badges, and success indicators, suggesting forensic certainty.
- **Tertiary (Gold/Ochre):** Used sparingly for high-value items, such as physical certificate identifiers, premium status, or "Limited Edition" markers.
- **Neutral:** A range of Slate greys (from `#F8FAFC` to `#64748B`) provides structural scaffolding without distracting from the artwork or certification data.
- **Background:** Pure White (`#FFFFFF`) ensures a clinical, distraction-free environment for inspecting high-resolution imagery.

## Typography

This design system uses a triple-font strategy to differentiate between narrative, data, and metadata.

- **Geist (Headings):** A clean, technical typeface that conveys precision. Use for all structural headings and page titles.
- **Inter (Body):** Selected for its high legibility in complex data environments. Use for all standard UI text, descriptions, and lists.
- **JetBrains Mono (Labels/Metadata):** A monospaced font used for forensic IDs, blockchain hashes, and technical timestamps. It reinforces the "high-security" and "forensic" nature of the platform.

## Layout & Spacing

The layout follows a **Fixed Grid** model for desktop to maintain a consistent, organized structure, transitioning to a fluid layout for mobile.

- **Desktop (1280px+):** 12-column grid with 24px gutters and 32px outer margins.
- **Tablet (768px - 1279px):** 8-column grid with 16px gutters and 24px margins.
- **Mobile (< 767px):** 4-column fluid grid with 12px gutters and 16px margins.

Spacing follows a strict 4px/8px incremental system. Components should prioritize vertical rhythm and generous padding within cards to prevent the "clinical" look from feeling "crowded."

## Elevation & Depth

Visual hierarchy is established through **Low-Contrast Outlines** and **Ambient Shadows**, inspired by modern professional tools.

- **Planes:** Surfaces are primarily flat, using subtle borders (`1px solid #E2E8F0`) to define boundaries.
- **Shadows:** Use extra-diffused, soft shadows for floating elements like dropdowns or active modals. Shadow color should be tinted with Primary Navy (`rgba(15, 23, 42, 0.08)`) to maintain color harmony.
- **Z-Axis:** 
    - Level 0: Pure White Background.
    - Level 1: Neutral Grey (`#F8FAFC`) cards/containers.
    - Level 2: Raised elements with soft shadows for focus.

## Shapes

The shape language uses **Rounded (2)** settings, specifically utilizing `2xl` (1.5rem) for large containers and `lg` (1rem) for standard components. This softens the technical aesthetic, making the platform feel sophisticated and premium rather than purely industrial.

- **Containers:** 24px (1.5rem) corner radius.
- **Buttons/Inputs:** 12px (0.75rem) corner radius.
- **Checkboxes:** 4px (0.25rem) corner radius for a sharp, precise look.

## Components

### Buttons & Chips
- **Primary:** Deep Navy background, white Geist text. Hover state shifts to a slightly lighter Navy.
- **Secondary:** Tech Green background for "Approve" or "Verify" actions.
- **Tertiary/Ghost:** Border only (`1px solid #E2E8F0`) with Inter text.
- **Security State:** Disabled buttons must include a small "padlock" icon to the left of the label, signaling a security lock rather than just a broken state.

### Input Fields
- Clean borders with a 2px focus ring in Primary Navy.
- Labels use **Inter SemiBold** for readability.
- Forensic inputs (IDs/Hashes) should use **JetBrains Mono**.

### Cards
- White background with a subtle `#F1F5F9` border.
- 24px padding internal.
- Header sections within cards should have a thin bottom-border to separate metadata from the content body.

### Status Indicators
- **Verified:** Tech Green chip with a checkmark icon.
- **Pending:** Gold/Ochre dot with a "Processing" label.
- **Warning/Alert:** Red-Orange accent for forensic inconsistencies.