# Interaction Reference

> Micro-interactions extracted from live DOM. Recreate these exactly for authentic feel.

## Coverage

| Component Type | Count | States Captured |
|----------------|-------|----------------|
| Button | 1 | default, hover, focus |
| Link | 3 | default, hover, focus |
| Input | 2 | default, hover, focus |

## Transition System

These transition declarations were extracted from interactive elements:

```css
transition: transform 0.25s, box-shadow 0.25s;
transition: all;
```

Apply these to all interactive elements. Never invent new durations or easings.

## Button Interactions

### Button 1 — `VER PLANES DISPONIBLES`

**States:**

- Default: `../screens/states/button-1-default.png`
- Hover: `../screens/states/button-1-hover.png`
- Focus: `../screens/states/button-1-focus.png`

**On hover:**

```css
/* box-shadow: rgba(79, 70, 229, 0.45) 0px 8px 30px 0px → */ box-shadow: rgba(124, 58, 237, 0.6) 0px 14px 40px 0px;
/* transform: none → */ transform: matrix(1, 0, 0, 1, 0, -2);
```

**On focus:**

```css
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `transform 0.25s, box-shadow 0.25s`

## Link Interactions

### Link 1 — `LLAMA AHORA`

**States:**

- Default: `../screens/states/link-1-default.png`
- Hover: `../screens/states/link-1-hover.png`
- Focus: `../screens/states/link-1-focus.png`

**On hover:**

```css
/* box-shadow: rgba(124, 58, 237, 0.55) 0px 14px 40px 0px → */ box-shadow: rgba(168, 85, 247, 0.65) 0px 18px 50px 0px;
/* transform: matrix(1, 0, 0, 1, 0, 0) → */ transform: matrix(1, 0, 0, 1, -108.586, -3);
```

**On focus:**

```css
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `transform 0.25s, box-shadow 0.25s`

### Link 2 — `LLÁMANOS AHORA`

**States:**

- Default: `../screens/states/link-2-default.png`
- Hover: `../screens/states/link-2-hover.png`
- Focus: `../screens/states/link-2-focus.png`

**On hover:**

```css
/* box-shadow: rgba(124, 58, 237, 0.28) 0px 6px 18px 0px → */ box-shadow: rgba(168, 85, 247, 0.45) 0px 10px 26px 0px;
```

**On focus:**

```css
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

### Link 3 — `VER DETALLES`

**States:**

- Default: `../screens/states/link-3-default.png`
- Hover: `../screens/states/link-3-hover.png`
- Focus: `../screens/states/link-3-focus.png`

**On hover:**

```css
/* background-color: rgba(34, 211, 238, 0.14) → */ background-color: rgba(34, 211, 238, 0.28);
/* color: rgb(14, 116, 144) → */ color: rgb(12, 74, 110);
/* outline: rgb(14, 116, 144) none 3px → */ outline: rgb(12, 74, 110) none 3px;
/* outline-color: rgb(14, 116, 144) → */ outline-color: rgb(12, 74, 110);
```

**On focus:**

```css
/* outline: rgb(14, 116, 144) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(14, 116, 144) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

## Input Interactions

### Input 1 — `Ingresa tu código ZIP`

**States:**

- Default: `../screens/states/input-1-default.png`
- Hover: `../screens/states/input-1-hover.png`
- Focus: `../screens/states/input-1-focus.png`

**Transition:** `all`

_No visible style changes detected for this element._

### Input 2 — `range`

**States:**

- Default: `../screens/states/input-2-default.png`
- Hover: `../screens/states/input-2-hover.png`
- Focus: `../screens/states/input-2-focus.png`

**On focus:**

```css
/* outline: rgb(157, 150, 142) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(157, 150, 142) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

## Interaction Rules

- Accent color `#06b6d4` is used for focus rings, active states, and hover highlights
- Hover effects include **color transitions** — use the extracted values, not approximations
- Focus states use **outline** (not box-shadow) — always match the extracted focus ring
- Transition durations in use: `0.25s`
- Always respect `prefers-reduced-motion` — set all transitions to `0s` when enabled

