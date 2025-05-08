# Salt Design System - Curve Variables

## Overview

Curve variables in the Salt Design System define border radius values that can be used to create consistent rounded corners across your application. These variables scale according to the selected density, allowing your UI to maintain appropriate styling across different device types and screen sizes.

## Curve Variables

All curve values are expressed in pixels and scale based on the density setting.

| Variable | Description |
|----------|-------------|
| `--salt-curve-0` | No curve (square corners) |
| `--salt-curve-50` | Extra small curve |
| `--salt-curve-100` | Small curve |
| `--salt-curve-150` | Medium-small curve |
| `--salt-curve-200` | Medium curve |
| `--salt-curve-250` | Large curve |
| `--salt-curve-999` | Pill shape (fully rounded) |

## Curve Values by Density

The curve variables scale proportionally based on the selected density. Here are the specific pixel values for each density:

### High Density (`salt-density-high`)

| Variable | Value |
|----------|-------|
| `--salt-curve-0` | 0 |
| `--salt-curve-50` | 1px |
| `--salt-curve-100` | 2px |
| `--salt-curve-150` | 3px |
| `--salt-curve-200` | 4px |
| `--salt-curve-250` | 5px |
| `--salt-curve-999` | 999px |

### Medium Density (`salt-density-medium`)

| Variable | Value |
|----------|-------|
| `--salt-curve-0` | 0 |
| `--salt-curve-50` | 2px |
| `--salt-curve-100` | 4px |
| `--salt-curve-150` | 6px |
| `--salt-curve-200` | 8px |
| `--salt-curve-250` | 10px |
| `--salt-curve-999` | 999px |

### Low Density (`salt-density-low`)

| Variable | Value |
|----------|-------|
| `--salt-curve-0` | 0 |
| `--salt-curve-50` | 3px |
| `--salt-curve-100` | 6px |
| `--salt-curve-150` | 9px |
| `--salt-curve-200` | 12px |
| `--salt-curve-250` | 15px |
| `--salt-curve-999` | 999px |

### Touch Density (`salt-density-touch`)

| Variable | Value |
|----------|-------|
| `--salt-curve-0` | 0 |
| `--salt-curve-50` | 4px |
| `--salt-curve-100` | 8px |
| `--salt-curve-150` | 12px |
| `--salt-curve-200` | 16px |
| `--salt-curve-250` | 20px |
| `--salt-curve-999` | 999px |

## Scaling Pattern

The curve variables follow a clear scaling pattern across densities:

1. **High Density**: Base values (smallest)
2. **Medium Density**: 2× high density values
3. **Low Density**: 3× high density values (for curve-50), 1.5× medium density values
4. **Touch Density**: 4× high density values (for curve-50), 2× medium density values

## Usage

Use curve variables in your CSS to create consistent rounded corners:

```css
.card {
  border-radius: var(--salt-curve-100);
}

.pill-button {
  border-radius: var(--salt-curve-999);
}

.subtle-panel {
  border-radius: var(--salt-curve-50);
}
```

## Density Classes

To apply a specific density to a component or container, use one of the following CSS classes:

- `.salt-density-touch` - For touch interfaces (largest curves)
- `.salt-density-low` - For lower density interfaces
- `.salt-density-medium` - For medium density interfaces
- `.salt-density-high` - For high density interfaces (smallest curves)

Example:
```html
<div class="salt-density-medium">
  <!-- Components inside will use medium density curves -->
  <button class="rounded-button">Click me</button>
</div>
```

## Best Practices

1. Always use curve variables instead of hardcoded pixel values
2. Select the appropriate curve size based on the UI element's purpose and visual hierarchy
3. Consider how curves will appear at different density settings
4. For related UI elements, maintain consistent curve values for visual harmony 