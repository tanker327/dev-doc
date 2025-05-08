# Salt Design System - Z-Index Variables

## Overview

Z-index variables in the Salt Design System provide a standardized way to control the stacking order of UI elements. These variables ensure that components stack consistently across your application, eliminating z-index conflicts and maintaining a predictable layering system.

## Z-Index Variables

The Salt Design System defines a hierarchical set of z-index values:

| Variable | Value | Description |
|----------|-------|-------------|
| `--salt-zIndex-default` | 1 | Base z-index for most elements |
| `--salt-zIndex-popout` | 1000 | For elements that appear above the main content |
| `--salt-zIndex-appHeader` | 1100 | Application headers that stay visible |
| `--salt-zIndex-drawer` | 1200 | Side drawers and panels |
| `--salt-zIndex-modal` | 1300 | Modal dialogs |
| `--salt-zIndex-notification` | 1400 | Notification elements |
| `--salt-zIndex-dragObject` | 1420 | Elements being dragged |
| `--salt-zIndex-contextMenu` | 1450 | Context menus |
| `--salt-zIndex-flyover` | 1500 | Tooltips and other flyover elements |

## Stacking Hierarchy

The z-index variables establish a clear stacking hierarchy:

1. **Default Content (1)**: Regular page content and UI elements
2. **Popout Elements (1000)**: Dropdown menus, comboboxes, popovers
3. **App Header (1100)**: Fixed application header/navigation bars
4. **Drawers (1200)**: Side panels and navigation drawers
5. **Modals (1300)**: Dialog boxes and modal windows
6. **Notifications (1400)**: Toast notifications, alerts
7. **Drag Objects (1420)**: Elements currently being dragged
8. **Context Menus (1450)**: Right-click menus
9. **Flyovers (1500)**: Tooltips, help text, quick info

This hierarchy ensures that more important UI elements (like tooltips) will always appear above less important ones (like dropdowns).

## Usage Examples

### Basic Usage

```css
.regular-content {
  z-index: var(--salt-zIndex-default);
}

.dropdown-menu {
  z-index: var(--salt-zIndex-popout);
}

.header-bar {
  z-index: var(--salt-zIndex-appHeader);
}

.side-panel {
  z-index: var(--salt-zIndex-drawer);
}

.dialog-window {
  z-index: var(--salt-zIndex-modal);
}

.toast-message {
  z-index: var(--salt-zIndex-notification);
}

.dragged-item {
  z-index: var(--salt-zIndex-dragObject);
}

.context-menu {
  z-index: var(--salt-zIndex-contextMenu);
}

.tooltip {
  z-index: var(--salt-zIndex-flyover);
}
```

### Relative Z-Index Values

You can also create relative z-index values within a stacking context:

```css
.dropdown-container {
  position: relative;
}

.dropdown-toggle {
  z-index: calc(var(--salt-zIndex-popout) + 1);
}

.dropdown-menu {
  z-index: var(--salt-zIndex-popout);
}
```

## Best Practices

1. Always use the z-index variables instead of hardcoded values
2. Choose the appropriate z-index variable based on the UI element's function, not just its visual appearance
3. Be cautious when creating new stacking contexts with `position` properties, as they can affect how z-index values work
4. For custom components, use z-index values that align with the existing hierarchy
5. When multiple elements use the same z-index, consider their DOM order (later elements stack on top)
6. For elements that need subtle variations within the same category, use calculations:
   ```css
   .tooltip-standard {
     z-index: var(--salt-zIndex-flyover);
   }
   .tooltip-important {
     z-index: calc(var(--salt-zIndex-flyover) + 10);
   }
   ```

## Density Support

These z-index variables are available in all density modes:
- `.salt-density-touch`
- `.salt-density-low`
- `.salt-density-medium`
- `.salt-density-high`

The z-index values remain consistent across density settings to ensure predictable stacking regardless of the UI density. 