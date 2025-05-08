# Salt Design System - Duration Variables

## Overview

Duration variables in the Salt Design System define standard time periods for animations and transitions. Using consistent durations helps create a cohesive feel across your application's interactive elements.

## Duration Variables

The Salt Design System provides a set of predefined duration variables that can be used for animations, transitions, and other time-based interactions:

| Variable | Value | Description |
|----------|-------|-------------|
| `--salt-duration-instant` | 0ms | Immediate transition with no animation |
| `--salt-duration-perceptible` | 300ms | Standard duration for most UI transitions |
| `--salt-duration-notable` | 1000ms | Longer duration for more significant transitions |
| `--salt-duration-cutoff` | 10000ms | Maximum duration for any animation (10 seconds) |

## Usage Guidelines

### When to Use Each Duration

- **Instant (0ms)**
  - Use for changes that should appear immediately
  - Appropriate for critical state changes where feedback should not be delayed
  - Examples: Toggle states that need immediate feedback

- **Perceptible (300ms)**
  - Standard duration for most UI animations
  - Fast enough to be responsive but long enough to be noticeable
  - Examples: Button hover states, dropdown menus, fade effects, slides

- **Notable (1000ms)**
  - Use for more significant UI changes that should draw user attention
  - Appropriate for bigger transitions or first-time information
  - Examples: Page transitions, welcome screens, celebratory animations

- **Cutoff (10000ms)**
  - Primarily used as a maximum threshold rather than an actual animation duration
  - Ensures that no animation exceeds a reasonable time limit
  - Useful as a fallback maximum duration

## Usage Examples

### Basic Transitions

```css
.button {
  transition: background-color var(--salt-duration-perceptible) ease-in-out;
}

.page-transition {
  transition: opacity var(--salt-duration-notable) ease;
}
```

### With Animation Variables

```css
.custom-animation {
  animation-duration: var(--salt-duration-perceptible);
  animation-timing-function: ease-in-out;
}
```

### Combining with Animation Variables

Salt Design System animations typically use these duration variables by default:

```css
/* The animation duration is set to var(--salt-duration-perceptible) */
.enter-animation {
  animation: var(--salt-animation-fade-in-forward);
}
```

## Accessibility Considerations

When using durations for animations and transitions, consider users who may have vestibular disorders or motion sensitivity:

1. For essential animations, keep durations short (prefer `--salt-duration-perceptible`)
2. For larger or full-screen animations, provide a way for users to reduce or disable animations
3. Respect user preferences set via the `prefers-reduced-motion` media query:

```css
@media (prefers-reduced-motion: reduce) {
  .animated-element {
    transition-duration: var(--salt-duration-instant) !important;
    animation-duration: var(--salt-duration-instant) !important;
  }
}
```

## Best Practices

1. Use the predefined duration variables instead of hardcoded time values
2. Match the duration to the importance and size of the UI change
3. For related animations, use the same duration for visual cohesion
4. Consider performance implications for animations on lower-powered devices 