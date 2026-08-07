# Animation Reference

> Cinematic motion design extracted from live DOM. Follow these specs exactly to recreate the experience.

## Motion Technology Stack

| Library | Type | Notes |
|---------|------|-------|
| **Web Animations API (65 active)** | animation |  |

## Scroll Journey

The page is **4,256px** tall. Each frame below shows what the user sees at that scroll depth.

> **Use these screenshots to understand WHAT animates, WHEN it animates, and HOW it moves.**

### 0% — Top / Hero
Scroll position: 0px

![Scroll 0%](../screens/scroll/scroll-000.png)

### 17% — Opening Section
Scroll position: 571px

![Scroll 17%](../screens/scroll/scroll-017.png)

### 33% — First Feature Section
Scroll position: 1,107px

![Scroll 33%](../screens/scroll/scroll-033.png)

### 50% — Mid-Page
Scroll position: 1,678px

![Scroll 50%](../screens/scroll/scroll-050.png)

### 67% — Lower Content
Scroll position: 2,249px

![Scroll 67%](../screens/scroll/scroll-067.png)

### 83% — Near Footer
Scroll position: 2,785px

![Scroll 83%](../screens/scroll/scroll-083.png)

### 100% — Bottom / Footer
Scroll position: 3,356px

![Scroll 100%](../screens/scroll/scroll-100.png)

## Scroll Animation Patterns

| Pattern | Library | Element Count | Duration | Delay | Easing |
|---------|---------|---------------|----------|-------|--------|
| parallax / sticky scroll | CSS | 1 | — | — | — |

### CSS Implementation

## CSS Keyframes (12 extracted)

### `@keyframes sc-shine`

Duration: `1.4s` · Easing: `ease` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `html.sc-dc-streaming .sc-placeholder::before, html.sc-dc-streaming .sc-interp.sc`

```css
@keyframes sc-shine {
  0% {
    background-position-x: 100%;
    background-position-y: 50%;
  }
  100% {
    background-position-x: 0%;
    background-position-y: 50%;
  }
}
```

> Background color/gradient shift · Background position (shimmer/scroll)

### `@keyframes floaty`

```css
@keyframes floaty {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-14px);
  }
}
```

> Transform/motion animation

### `@keyframes floaty2`

```css
@keyframes floaty2 {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(12px);
  }
}
```

> Transform/motion animation

### `@keyframes breathe`

```css
@keyframes breathe {
  0%, 100% {
    opacity: 0.45;
    transform: scale(1);
  }
  50% {
    opacity: 0.85;
    transform: scale(1.06);
  }
}
```

> Fade + motion enter animation

### `@keyframes orbit`

```css
@keyframes orbit {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes marquee`

```css
@keyframes marquee {
  0% {
    transform: translateX(0px);
  }
  100% {
    transform: translateX(-50%);
  }
}
```

> Transform/motion animation

### `@keyframes sweep`

```css
@keyframes sweep {
  0% {
    transform: translateX(-120%);
  }
  60%, 100% {
    transform: translateX(220%);
  }
}
```

> Transform/motion animation

### `@keyframes zeReveal`

```css
@keyframes zeReveal {
  0% {
    opacity: 0;
    transform: translateY(26px) scale(0.985);
    filter: blur(7px);
  }
  100% {
    opacity: 1;
    transform: none;
    filter: blur(0px);
  }
}
```

> Fade + motion enter animation · Filter effect (blur/brightness)

### `@keyframes zeDrop`

```css
@keyframes zeDrop {
  0% {
    opacity: 0;
    transform: translateY(-16px) scale(0.9);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes zeBgSettle`

```css
@keyframes zeBgSettle {
  0% {
    opacity: 0;
    transform: scale(1.12);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zePop`

```css
@keyframes zePop {
  0% {
    opacity: 0;
    transform: translateY(8px) scale(0.78);
  }
  70% {
    opacity: 1;
    transform: scale(1.07);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes pulsering`

```css
@keyframes pulsering {
  0% {
    transform: scale(0.9);
    opacity: 0.7;
  }
  100% {
    transform: scale(1.7);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

## How to Recreate This Motion Design

### Step 1 — Install Dependencies

```bash
```

### Step 2 — Scroll-Reveal Pattern

Elements that animate into view follow this pattern:

```css
/* Initial hidden state */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.6s cubic-bezier(0.4, 0, 0.2, 1),
              transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

### Step 3 — Key Motion Principles

- **Always add** `@media (prefers-reduced-motion: reduce) { * { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; } }`

### Step 4 — Scroll Journey Reference

Match what happens at each scroll position:

- **0%** (`0px`) → `screens/scroll/scroll-000.png`
- **17%** (`571px`) → `screens/scroll/scroll-017.png`
- **33%** (`1107px`) → `screens/scroll/scroll-033.png`
- **50%** (`1678px`) → `screens/scroll/scroll-050.png`
- **67%** (`2249px`) → `screens/scroll/scroll-067.png`
- **83%** (`2785px`) → `screens/scroll/scroll-083.png`
- **100%** (`3356px`) → `screens/scroll/scroll-100.png`

