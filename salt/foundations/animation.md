# Salt Design System - Animation Variables

## Overview

The Salt Design System provides a comprehensive set of animation variables to ensure consistent motion across your application. These animations are designed to enhance user experience with smooth, predictable transitions.

## Animation Base Variables

These variables define the fundamental properties used in all animations:

| Variable | Description | Default Value |
|----------|-------------|---------------|
| `--salt-animation-opacity-start` | Starting opacity for fade animations | 0 |
| `--salt-animation-opacity-end` | Ending opacity for fade animations | 1 |
| `--salt-animation-scale-start` | Starting scale for scale animations | 0 |
| `--salt-animation-scale-end` | Ending scale for scale animations | 1 |
| `--salt-animation-transform-start` | Starting transform displacement | 100% |
| `--salt-animation-transform-end` | Ending transform displacement | 0 |
| `--salt-animation-duration` | Default animation duration | var(--salt-duration-perceptible) (300ms) |
| `--salt-animation-timing-function` | Default timing function | ease-in-out |

## Animation Types

### Slide Animations

Slide animations move elements into or out of view with a combined translation and fade effect.

#### Slide In

| Variable | Description | Applied Animation |
|----------|-------------|-------------------|
| `--salt-animation-slide-in-top` | Slide in from the top | slide-in-top with defined duration and timing |
| `--salt-animation-slide-in-left` | Slide in from the left | slide-in-left with defined duration and timing |
| `--salt-animation-slide-in-right` | Slide in from the right | slide-in-right with defined duration and timing |
| `--salt-animation-slide-in-bottom` | Slide in from the bottom | slide-in-bottom with defined duration and timing |

#### Slide Out

| Variable | Description | Applied Animation |
|----------|-------------|-------------------|
| `--salt-animation-slide-out-top` | Slide out to the top | slide-out-top with defined duration and timing (including 'both' fill mode) |
| `--salt-animation-slide-out-left` | Slide out to the left | slide-out-left with defined duration and timing (including 'both' fill mode) |
| `--salt-animation-slide-out-right` | Slide out to the right | slide-out-right with defined duration and timing (including 'both' fill mode) |
| `--salt-animation-slide-out-bottom` | Slide out to the bottom | slide-out-bottom with defined duration and timing (including 'both' fill mode) |

### Fade Animations

Fade animations change opacity and sometimes scale to create smooth transitions.

| Variable | Description | Applied Animation |
|----------|-------------|-------------------|
| `--salt-animation-fade-in-back` | Fade in with scale down (from larger) | fade-in-back with defined duration and timing |
| `--salt-animation-fade-in-forward` | Fade in with scale up (from smaller) | fade-in-forward with defined duration and timing |
| `--salt-animation-fade-in-center` | Fade in without scaling | fade-in-center with defined duration and timing |
| `--salt-animation-fade-out-back` | Fade out without scaling | fade-out-back with defined duration and timing (including 'both' fill mode) |

## Keyframe Animations

The Salt Design System includes predefined keyframe animations that power the animation variables:

### Slide Keyframes

| Animation Name | Description | Behavior |
|----------------|-------------|----------|
| `slide-in-top` | Animate entry from the top | Fades in and translates from top to center |
| `slide-out-top` | Animate exit to the top | Fades out and translates from center to top |
| `slide-in-left` | Animate entry from the left | Fades in and translates from left to center |
| `slide-out-left` | Animate exit to the left | Fades out and translates from center to left |
| `slide-in-right` | Animate entry from the right | Fades in and translates from right to center |
| `slide-out-right` | Animate exit to the right | Fades out and translates from center to right |
| `slide-in-bottom` | Animate entry from the bottom | Fades in and translates from bottom to center |
| `slide-out-bottom` | Animate exit to the bottom | Fades out and translates from center to bottom |

### Fade Keyframes

| Animation Name | Description | Behavior |
|----------------|-------------|----------|
| `fade-in-back` | Animate entry with scale down | Starts at larger scale (1.4) and opacity 0, animates to normal scale and full opacity |
| `fade-in-forward` | Animate entry with scale up | Starts at smaller scale (0.6) and opacity 0, animates to normal scale and full opacity |
| `fade-in-center` | Simple fade in | Animates from opacity 0 to opacity 1 without scaling |
| `fade-out-back` | Simple fade out | Animates from opacity 1a to opacity 0 without scaling |

## Usage

To apply animations to your elements, use the animation variables in your CSS:

```css
.modal-enter {
  animation: var(--salt-animation-fade-in-forward);
}

.modal-exit {
  animation: var(--salt-animation-fade-out-back);
}

.slide-element {
  animation: var(--salt-animation-slide-in-right);
}
```

### CSS Animation Properties

You can also customize animations further by using the base variables:

```css
.custom-animation {
  animation-name: slide-in-bottom;
  animation-duration: calc(2 * var(--salt-animation-duration));
  animation-timing-function: var(--salt-animation-timing-function);
  animation-fill-mode: both;
}
```

## Density Support

These animation variables are available in all density modes:
- `.salt-density-touch`
- `.salt-density-low`
- `.salt-density-medium`
- `.salt-density-high`

Animations will maintain consistent behavior regardless of the density setting, ensuring a unified experience across different device types and screen sizes. 