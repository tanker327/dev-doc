# Salt Design System - Size Variables

## Overview

Size variables in the Salt Design System define standardized dimensions for UI elements. These variables scale appropriately across different density modes, ensuring consistent proportions while optimizing for different device types and screen sizes.

## Size Variables

The Salt Design System provides the following size variables:

| Variable | Description |
|----------|-------------|
| `--salt-size-adornment` | Size for icon adornments in components |
| `--salt-size-bar` | Standard bar thickness (e.g., for progress bars) |
| `--salt-size-base` | Base height for interactive elements |
| `--salt-size-border` | Standard border width |
| `--salt-size-icon` | Standard icon size |
| `--salt-size-indicator` | Size for indicators (e.g., notification dots) |
| `--salt-size-selectable` | Size for selectable elements (e.g., checkboxes) |
| `--salt-size-bar-strong` | Thickness for more prominent bars |
| `--salt-size-bar-small` | Thickness for smaller, subtle bars |
| `--salt-size-border-strong` | Width for more prominent borders |

## Size Values by Density

These size variables scale according to the selected density, with larger values for lower densities:

### High Density (`salt-density-high`)

| Variable | Value |
|----------|-------|
| `--salt-size-adornment` | 6px |
| `--salt-size-bar` | 2px |
| `--salt-size-base` | 20px |
| `--salt-size-border` | 1px |
| `--salt-size-icon` | 10px |
| `--salt-size-indicator` | 2px |
| `--salt-size-selectable` | 12px |
| `--salt-size-bar-strong` | 4px |
| `--salt-size-bar-small` | 2px |
| `--salt-size-border-strong` | 2px |

### Medium Density (`salt-density-medium`)

| Variable | Value |
|----------|-------|
| `--salt-size-adornment` | 8px |
| `--salt-size-bar` | 4px |
| `--salt-size-base` | 28px |
| `--salt-size-border` | 1px |
| `--salt-size-icon` | 12px |
| `--salt-size-indicator` | 3px |
| `--salt-size-selectable` | 14px |
| `--salt-size-bar-strong` | 8px |
| `--salt-size-bar-small` | 2px |
| `--salt-size-border-strong` | 2px |

### Low Density (`salt-density-low`)

| Variable | Value |
|----------|-------|
| `--salt-size-adornment` | 10px |
| `--salt-size-bar` | 6px |
| `--salt-size-base` | 36px |
| `--salt-size-border` | 1px |
| `--salt-size-icon` | 14px |
| `--salt-size-indicator` | 4px |
| `--salt-size-selectable` | 16px |
| `--salt-size-bar-strong` | 12px |
| `--salt-size-bar-small` | 2px |
| `--salt-size-border-strong` | 2px |

### Touch Density (`salt-density-touch`)

| Variable | Value |
|----------|-------|
| `--salt-size-adornment` | 12px |
| `--salt-size-bar` | 8px |
| `--salt-size-base` | 44px |
| `--salt-size-border` | 1px |
| `--salt-size-icon` | 16px |
| `--salt-size-indicator` | 5px |
| `--salt-size-selectable` | 18px |
| `--salt-size-bar-strong` | 16px |
| `--salt-size-bar-small` | 2px |
| `--salt-size-border-strong` | 2px |

## Scaling Patterns

Most size variables follow consistent scaling patterns across densities:

1. **Base Size**: Increases by 8px increments from high to low density (20px → 28px → 36px → 44px)
2. **Icon Size**: Increases by 2px increments (10px → 12px → 14px → 16px)
3. **Bars**: Double in size between high and medium, and increase linearly after
4. **Selectable Elements**: Increase by 2px increments (12px → 14px → 16px → 18px)

Note that some values remain constant across densities, such as `--salt-size-border` (1px) and `--salt-size-bar-small` (2px).

## Usage Examples

### Basic Usage

```css
.custom-button {
  height: var(--salt-size-base);
  border-width: var(--salt-size-border);
}

.custom-icon {
  width: var(--salt-size-icon);
  height: var(--salt-size-icon);
}

.progress-indicator {
  height: var(--salt-size-bar);
}
```

### Adaptive Component Sizing

```css
.status-indicator {
  width: var(--salt-size-indicator);
  height: var(--salt-size-indicator);
  border-radius: 50%;
}

.checkbox {
  width: var(--salt-size-selectable);
  height: var(--salt-size-selectable);
}
```

## Density Classes

To apply a specific density to a component or container, use one of the following CSS classes:

- `.salt-density-touch` - For touch interfaces (largest sizes)
- `.salt-density-low` - For lower density interfaces
- `.salt-density-medium` - For medium density interfaces
- `.salt-density-high` - For high density interfaces (smallest sizes)

Example:
```html
<div class="salt-density-medium">
  <!-- Components inside will use medium density sizing -->
  <button class="custom-button">Click me</button>
</div>
```

## Best Practices

1. Always use size variables instead of hardcoded pixel values
2. Consider the appropriate density mode for your target devices:
   - Touch density for tablets and touchscreen devices
   - Low density for casual desktop usage
   - Medium density for professional desktop applications
   - High density for dense, information-rich interfaces
3. For custom components, maintain proportional sizing using these variables
4. When creating custom size tokens, follow the existing scaling patterns 