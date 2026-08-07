# connecting-live DESIGN.md

> Auto-generated design system — reverse-engineered via static analysis by skillui.
> Frameworks: None detected
> Colors: 20 · Fonts: 2 · Components: 7
> Icon library: not detected · State: not detected
> Primary theme: dark · Dark mode toggle: no · Motion: expressive

## Visual Reference

**Match this design exactly** — study colors, fonts, spacing, and component shapes before writing any UI code.

![connecting-live Homepage](../screenshots/homepage.png)

---

## 1. Visual Theme & Atmosphere

This is a **dark-themed** interface with a cool tone. Depth is expressed through layered shadows and subtle surface color variation. Typography pairs **Plus Jakarta Sans** for display/headings with **Outfit** for body text, creating clear visual hierarchy through type contrast. Spacing follows a **4px base grid** (compact density), with scale: 2, 4, 6, 8, 10, 12, 14, 16px. The palette is predominantly monochromatic with **#06b6d4** as the single accent color — used sparingly for interactive elements and emphasis. Motion is expressive — spring physics, layout animations, and staggered reveals are part of the visual language.

---

## 2. Color Palette & Roles

| Token | Hex | Role | Use |
|---|---|---|---|
| background | `#1b2233` | background | Page background, darkest surface |
| surface | `#0f172a` | surface | Card and panel backgrounds |
| text-primary | `#ffffff` | text-primary | Headings and body text |
| text-muted | `#6b7890` | text-muted | Captions, placeholders, secondary info |
| accent | `#06b6d4` | accent | CTAs, links, focus rings, active states |
| danger | `#ef4444` | danger | Error states, destructive actions |
| info | `#22d3ee` | info | Informational highlights |
| unknown | `#3c4a63` | unknown | Palette color |
| unknown | `#56637d` | unknown | Palette color |
| unknown | `#2f3b52` | unknown | Palette color |
| unknown | `#a855f7` | unknown | Palette color |
| unknown | `#0e7490` | unknown | Palette color |
| unknown | `#7c3aed` | unknown | Palette color |
| unknown | `#e879f9` | unknown | Palette color |
| unknown | `#4b5a75` | unknown | Palette color |
| unknown | `#3b82f6` | unknown | Palette color |
| unknown | `#2563eb` | unknown | Palette color |
| unknown | `#0891b2` | unknown | Palette color |
| unknown | `#1d4ed8` | unknown | Palette color |
| unknown | `#d946ef` | unknown | Palette color |


---

## 3. Typography Rules

**Font Stack:**
- **Outfit** — Heading 1, Heading 2, Heading 3
- **Plus Jakarta Sans** — Body, Caption

**Font Sources:**

```css
@font-face {
  font-family: "Outfit";
  src: url("fonts/Outfit-SemiBold.ttf") format("truetype");
  font-weight: 600;
}
@font-face {
  font-family: "Outfit";
  src: url("fonts/Outfit-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Outfit";
  src: url("fonts/Outfit-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "Plus Jakarta Sans";
  src: url("fonts/PlusJakartaSans-SemiBold.ttf") format("truetype");
  font-weight: 600;
}
@font-face {
  font-family: "Plus Jakarta Sans";
  src: url("fonts/PlusJakartaSans-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Plus Jakarta Sans";
  src: url("fonts/PlusJakartaSans-Regular.ttf") format("truetype");
  font-weight: 400;
}
```

| Role | Font | Size | Weight |
|---|---|---|---|
| Heading 1 | Outfit | 48px / 3rem | 700 |
| Heading 2 | Outfit | 32px / 2rem | 600 |
| Heading 3 | Outfit | 24px / 1.5rem | 600 |
| Body | Plus Jakarta Sans | 16px / 1rem | 400 |
| Caption | Plus Jakarta Sans | 12px / 0.75rem | 400 |

**Typographic Rules:**
- Limit to 2 font families max per screen
- Use **Outfit** for body/UI text, **Plus Jakarta Sans** for display/headings
- Maintain consistent hierarchy: no more than 3-4 font sizes per screen
- Headings use bold (600-700), body uses regular (400)
- Line height: 1.5 for body text, 1.2 for headings
- Use color and opacity for secondary hierarchy, not additional font sizes


---

## 4. Component Stylings

### Layout (1)

**Footer** — `html`

### Navigation (1)

**Navigation** — `html`

### Data Display (1)

**List** — `html`

### Data Input (2)

**Button** — `html`

**Input** — `html`
- State: :focus, :placeholder

### Media (2)

**Image** — `html`

**Icon** — `html`



---

## 5. Layout Principles

- **Base spacing unit:** 4px
- **Spacing scale:** 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24
- **Border radius:** 12px, 18px, 20px, 24px, 999px
- **Max content width:** 960px

**Spacing as Meaning:**
| Spacing | Use |
|---|---|
| 4-8px | Tight: related items within a group |
| 12-16px | Medium: between groups |
| 24-32px | Wide: between sections |
| 48px+ | Vast: major section breaks |


---

## 6. Depth & Elevation

### Floating — dropdowns, popovers, modals

- `rgba(124, 58, 237, 0.28) 0px 6px 18px 0px`
- `rgba(6, 182, 212, 0.8) 0px 0px 12px 0px`
- `rgb(34, 211, 238) 0px 0px 20px 0px`

### Overlay — full-screen overlays, top-level dialogs

- `rgba(124, 58, 237, 0.55) 0px 14px 40px 0px`
- `rgba(168, 85, 247, 0.45) 0px 10px 30px 0px`
- `rgba(168, 85, 247, 0.5) 0px 12px 36px 0px`



---

## 7. Animation & Motion

This project uses **expressive motion**. Animations are an integral part of the experience.

### CSS Animations

- `@keyframes floaty`
- `@keyframes floaty2`
- `@keyframes breathe`
- `@keyframes orbit`
- `@keyframes marquee`
- `@keyframes sweep`
- `@keyframes zeReveal`
- `@keyframes zeDrop`

### Motion Guidelines

- Duration: 150-300ms for micro-interactions, 300-500ms for page transitions
- Easing: `ease-out` for enters, `ease-in` for exits
- Always respect `prefers-reduced-motion`


---

## 8. Do's and Don'ts

### Do's

- Use `#06b6d4` for interactive elements (buttons, links, focus rings)
- Use `#1b2233` as the primary page background
- Pair **Outfit** (body) with **Plus Jakarta Sans** (display) — these are the only allowed fonts
- Follow the **4px** spacing grid for all margins, padding, and gaps
- Use the defined shadow tokens for elevation — see Section 6
- Use border-radius from the scale: 12px, 18px, 20px, 24px, 999px
- Reuse existing components from Section 4 before creating new ones

### Don'ts

- Don't introduce colors outside this palette — extend the design tokens first
- Don't introduce additional font families beyond Outfit and Plus Jakarta Sans
- Don't use arbitrary spacing values — stick to multiples of 4px
- Don't create custom box-shadow values outside the system tokens
- Don't use gradients — the design uses solid colors only
- Don't use arbitrary border-radius values — pick from the defined scale
- Don't duplicate component patterns — check Section 4 first
- Don't use backdrop-blur or blur effects

### Anti-Patterns (detected from codebase)

- No gradient backgrounds
- No blur or backdrop-blur effects
- No zebra striping on tables/lists


---

## 9. Responsive Behavior

| Name | Value | Source |
|---|---|---|
| xs | 420px | css |
| sm | 640px | css |
| lg | 960px | css |

**Approach:** Use `@media (min-width: ...)` queries matching the breakpoints above.


---

## 10. Agent Prompt Guide

Use these as starting points when building new UI:

### Build a Card

```
Background: #0f172a
Border: 1px solid var(--border)
Radius: 20px
Padding: 16px
Font: Outfit
Use shadow tokens from Section 6.
```

### Build a Button

```
Primary: bg #06b6d4, text white
Ghost: bg transparent, border var(--border)
Padding: 8px 16px
Radius: 20px
Hover: opacity 0.9 or lighter shade
Focus: ring with #06b6d4
```

### Build a Page Layout

```
Background: #1b2233
Max-width: 960px, centered
Grid: 4px base
Responsive: mobile-first, breakpoints from Section 9
```

### Build a Stats Card

```
Surface: #0f172a
Label: #6b7890 (muted, 12px, uppercase)
Value: #ffffff (primary, 24-32px, bold)
Status: use success/warning/danger from Section 2
```

### Build a Form

```
Input bg: #1b2233
Input border: 1px solid var(--border)
Focus: border-color #06b6d4
Label: #6b7890 12px
Spacing: 16px between fields
Radius: 20px
```

### General Component

```
1. Read DESIGN.md Sections 2-6 for tokens
2. Colors: only from palette
3. Font: Outfit, type scale from Section 3
4. Spacing: 4px grid
5. Components: match patterns from Section 4
6. Elevation: shadow tokens
```
