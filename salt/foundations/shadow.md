# Salt Design System - Shadow Variables

## Overview

Shadow variables in the Salt Design System provide consistent elevation effects across your application. These shadows are designed to create depth and hierarchy in your user interface, with variations for both light and dark color modes.

## Shadow Variables

The Salt Design System provides five levels of shadow intensity, each defined with appropriate colors and offsets:

| Variable | Light Mode | Dark Mode | Description |
|----------|------------|-----------|-------------|
| `--salt-shadow-100` | 0 1px 3px 0 rgba(0, 0, 0, 0.1) | 0 1px 3px 0 rgba(0, 0, 0, 0.5) | Subtle shadow for slight elevation |
| `--salt-shadow-200` | 0 2px 4px 0 rgba(0, 0, 0, 0.1) | 0 2px 4px 0 rgba(0, 0, 0, 0.5) | Light shadow for low elevation |
| `--salt-shadow-300` | 0 4px 8px 0 rgba(0, 0, 0, 0.15) | 0 4px 8px 0 rgba(0, 0, 0, 0.55) | Medium shadow for moderate elevation |
| `--salt-shadow-400` | 0 6px 10px 0 rgba(0, 0, 0, 0.2) | 0 6px 10px 0 rgba(0, 0, 0, 0.55) | Pronounced shadow for high elevation |
| `--salt-shadow-500` | 0 12px 40px 0 rgba(0, 0, 0, 0.3) | 0 12px 40px 0 rgba(0, 0, 0, 0.65) | Strong shadow for maximum elevation |

## Shadow Color Variables

The actual shadow colors are defined separately for light and dark modes:

### Light Mode (`data-mode="light"`)

| Variable | Value |
|----------|-------|
| `--salt-shadow-100-color` | rgba(0, 0, 0, 0.1) |
| `--salt-shadow-200-color` | rgba(0, 0, 0, 0.1) |
| `--salt-shadow-300-color` | rgba(0, 0, 0, 0.15) |
| `--salt-shadow-400-color` | rgba(0, 0, 0, 0.2) |
| `--salt-shadow-500-color` | rgba(0, 0, 0, 0.3) |

### Dark Mode (`data-mode="dark"`)

| Variable | Value |
|----------|-------|
| `--salt-shadow-100-color` | rgba(0, 0, 0, 0.5) |
| `--salt-shadow-200-color` | rgba(0, 0, 0, 0.5) |
| `--salt-shadow-300-color` | rgba(0, 0, 0, 0.55) |
| `--salt-shadow-400-color` | rgba(0, 0, 0, 0.55) |
| `--salt-shadow-500-color` | rgba(0, 0, 0, 0.65) |

## Usage Guidelines

### Elevation Hierarchy

Each shadow level is designed to represent a specific level of elevation in your UI:

- **Shadow 100**: Very subtle elevation, for elements that are just slightly raised
- **Shadow 200**: Light elevation, for elements that need to be distinguished but not prominent
- **Shadow 300**: Medium elevation, for interactive elements like cards or buttons
- **Shadow 400**: High elevation, for elements floating above the content like dropdowns or popovers
- **Shadow 500**: Maximum elevation, for elements like modals or dialogs that should dominate the view

### Mode-Specific Shadows

The shadow variables automatically adjust based on the `data-mode` attribute:

```html
<div class="salt-theme" data-mode="light">
  <!-- Light mode shadows will be used here -->
</div>

<div class="salt-theme" data-mode="dark">
  <!-- Dark mode shadows will be used here -->
</div>
```

## Usage Examples

### Basic Usage

```css
.card {
  box-shadow: var(--salt-shadow-300);
}

.dropdown {
  box-shadow: var(--salt-shadow-400);
}

.modal {
  box-shadow: var(--salt-shadow-500);
}
```

### Interactive Elements

You can combine shadows with transitions for interactive effects:

```css
.interactive-card {
  box-shadow: var(--salt-shadow-200);
  transition: box-shadow var(--salt-duration-perceptible) ease-in-out;
}

.interactive-card:hover {
  box-shadow: var(--salt-shadow-300);
}
```

## Best Practices

1. Use shadows consistently to establish a clear hierarchy in your UI
2. Match the shadow intensity to the element's importance and elevation
3. Avoid using multiple heavy shadows in the same view
4. Consider how shadows will appear in both light and dark modes
5. For interactive elements, consider increasing the shadow on hover/focus states 