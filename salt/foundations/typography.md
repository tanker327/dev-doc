# Salt Design System - Typography Variables

## Overview

Typography variables in the Salt Design System define the font families and font weights used across the design system. These variables ensure typographic consistency and help maintain the visual language of your application.

## Font Family Variables

The Salt Design System provides variables for three primary font families:

| Variable | Value | Description |
|----------|-------|-------------|
| `--salt-typography-fontFamily-openSans` | "Open Sans" | Primary sans-serif font for most text content |
| `--salt-typography-fontFamily-amplitude` | "Amplitude" | Display font typically used for headings and featured text |
| `--salt-typography-fontFamily-ptMono` | "PT Mono" | Monospace font used for code, technical content, and data |

## Font Weight Variables

The Salt Design System provides a comprehensive range of font weight variables:

| Variable | Value | CSS Weight Name | Description |
|----------|-------|----------------|-------------|
| `--salt-typography-fontWeight-light` | 300 | Light | Lighter than normal text |
| `--salt-typography-fontWeight-regular` | 400 | Regular/Normal | Standard text weight |
| `--salt-typography-fontWeight-medium` | 500 | Medium | Slightly heavier than regular |
| `--salt-typography-fontWeight-semiBold` | 600 | Semi-Bold | Semi-bold text weight |
| `--salt-typography-fontWeight-bold` | 700 | Bold | Bold text weight |
| `--salt-typography-fontWeight-extraBold` | 800 | Extra Bold | Extra bold weight for strong emphasis |

## Text Decoration Variables

The Salt Design System also includes variables for text decoration:

| Variable | Value | Description |
|----------|-------|-------------|
| `--salt-typography-textDecoration-none` | none | No text decoration |
| `--salt-typography-textDecoration-underline` | underline | Underlined text |

## Usage Examples

### Font Family Usage

```css
.text-content {
  font-family: var(--salt-typography-fontFamily-openSans);
}

.heading {
  font-family: var(--salt-typography-fontFamily-amplitude);
}

.code-block {
  font-family: var(--salt-typography-fontFamily-ptMono);
}
```

### Font Weight Usage

```css
.regular-text {
  font-weight: var(--salt-typography-fontWeight-regular);
}

.emphasized-text {
  font-weight: var(--salt-typography-fontWeight-medium);
}

.heading-primary {
  font-weight: var(--salt-typography-fontWeight-bold);
}

.heading-secondary {
  font-weight: var(--salt-typography-fontWeight-semiBold);
}

.subtle-text {
  font-weight: var(--salt-typography-fontWeight-light);
}
```

### Text Decoration Usage

```css
.link {
  text-decoration: var(--salt-typography-textDecoration-underline);
}

.link-hover {
  text-decoration: var(--salt-typography-textDecoration-none);
}
```

## Combining Typography Variables

Typography variables can be combined to create consistent text styles:

```css
.heading-primary {
  font-family: var(--salt-typography-fontFamily-amplitude);
  font-weight: var(--salt-typography-fontWeight-bold);
}

.body-text {
  font-family: var(--salt-typography-fontFamily-openSans);
  font-weight: var(--salt-typography-fontWeight-regular);
}

.code-example {
  font-family: var(--salt-typography-fontFamily-ptMono);
  font-weight: var(--salt-typography-fontWeight-regular);
}

.link {
  text-decoration: var(--salt-typography-textDecoration-underline);
  font-weight: var(--salt-typography-fontWeight-medium);
}
```

## Best Practices

1. Use the predefined typography variables instead of hardcoded values
2. Maintain a consistent typographic hierarchy using appropriate font weights
3. Limit the number of font weights used in a single interface to maintain visual cohesion
4. Use the appropriate font family for the content type:
   - Open Sans for general UI text
   - Amplitude for headings and featured text
   - PT Mono for code, data, and technical content
5. Consider accessibility when choosing font weights (ensure sufficient contrast)
6. Use underlines for interactive text elements like links 