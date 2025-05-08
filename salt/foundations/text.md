# Salt Design System - Text Characteristics

## Overview

The Salt Design System provides a comprehensive set of text variables for consistent typography across your application. These variables control font families, weights, sizes, and line heights for different text elements and scale appropriately across density settings.

## Text Categories

The text characteristics are organized into several categories:

- **Default/Body Text**: General purpose text styling
- **Action Text**: For buttons and interactive elements
- **Headings (H1-H4)**: Section titles of varying importance
- **Label Text**: For form labels and annotations
- **Display Text (Display1-4)**: Large, impactful text for hero sections
- **Notation Text**: For small, subsidiary text
- **Code Text**: For code snippets and technical content

## General Text Properties

| Variable | Description | Default Value |
|----------|-------------|---------------|
| `--salt-text-letterSpacing` | Letter spacing for most text | 0 |
| `--salt-text-textAlign` | Default text alignment | left |
| `--salt-text-textAlign-embedded` | Text alignment for embedded elements | center |

## Text Variables by Category

### Body Text

These variables apply to the default body text:

| Variable | Description |
|----------|-------------|
| `--salt-text-fontFamily` | Font family for body text |
| `--salt-text-fontWeight` | Regular font weight for body text |
| `--salt-text-fontWeight-small` | Light font weight for body text |
| `--salt-text-fontWeight-strong` | Bold font weight for body text |
| `--salt-text-fontSize` | Font size for body text (density-dependent) |
| `--salt-text-lineHeight` | Line height for body text (density-dependent) |
| `--salt-text-minHeight` | Minimum height for body text elements (density-dependent) |

### Action Text

These variables apply to interactive elements like buttons:

| Variable | Description |
|----------|-------------|
| `--salt-text-action-fontFamily` | Font family for actions |
| `--salt-text-action-letterSpacing` | Letter spacing for actions (0.6px) |
| `--salt-text-action-textTransform` | Text transformation for actions (uppercase) |
| `--salt-text-action-textAlign` | Text alignment for actions (center) |
| `--salt-text-action-fontWeight` | Regular font weight for actions |
| `--salt-text-action-fontWeight-small` | Light font weight for actions |
| `--salt-text-action-fontWeight-strong` | Bold font weight for actions |

### Headings

Variables for heading elements H1 through H4:

#### H1

| Variable | Description |
|----------|-------------|
| `--salt-text-h1-fontFamily` | Font family for H1 headings |
| `--salt-text-h1-fontWeight` | Regular font weight for H1 headings |
| `--salt-text-h1-fontWeight-small` | Light font weight for H1 headings |
| `--salt-text-h1-fontWeight-strong` | Bold font weight for H1 headings |
| `--salt-text-h1-fontSize` | Font size for H1 headings (density-dependent) |
| `--salt-text-h1-lineHeight` | Line height for H1 headings (density-dependent) |

#### H2

| Variable | Description |
|----------|-------------|
| `--salt-text-h2-fontFamily` | Font family for H2 headings |
| `--salt-text-h2-fontWeight` | Regular font weight for H2 headings |
| `--salt-text-h2-fontWeight-small` | Light font weight for H2 headings |
| `--salt-text-h2-fontWeight-strong` | Bold font weight for H2 headings |
| `--salt-text-h2-fontSize` | Font size for H2 headings (density-dependent) |
| `--salt-text-h2-lineHeight` | Line height for H2 headings (density-dependent) |

#### H3

| Variable | Description |
|----------|-------------|
| `--salt-text-h3-fontFamily` | Font family for H3 headings |
| `--salt-text-h3-fontWeight` | Regular font weight for H3 headings |
| `--salt-text-h3-fontWeight-small` | Light font weight for H3 headings |
| `--salt-text-h3-fontWeight-strong` | Bold font weight for H3 headings |
| `--salt-text-h3-fontSize` | Font size for H3 headings (density-dependent) |
| `--salt-text-h3-lineHeight` | Line height for H3 headings (density-dependent) |

#### H4

| Variable | Description |
|----------|-------------|
| `--salt-text-h4-fontFamily` | Font family for H4 headings |
| `--salt-text-h4-fontWeight` | Regular font weight for H4 headings |
| `--salt-text-h4-fontWeight-small` | Light font weight for H4 headings |
| `--salt-text-h4-fontWeight-strong` | Bold font weight for H4 headings |
| `--salt-text-h4-fontSize` | Font size for H4 headings (density-dependent) |
| `--salt-text-h4-lineHeight` | Line height for H4 headings (density-dependent) |

### Label Text

| Variable | Description |
|----------|-------------|
| `--salt-text-label-fontFamily` | Font family for labels |
| `--salt-text-label-fontWeight` | Regular font weight for labels |
| `--salt-text-label-fontWeight-small` | Light font weight for labels |
| `--salt-text-label-fontWeight-strong` | Bold font weight for labels |
| `--salt-text-label-fontSize` | Font size for labels (density-dependent) |
| `--salt-text-label-lineHeight` | Line height for labels (density-dependent) |

### Display Text

Variables for large, impactful display text:

#### Display1 (Largest)

| Variable | Description |
|----------|-------------|
| `--salt-text-display1-fontFamily` | Font family for Display1 text |
| `--salt-text-display1-fontWeight` | Regular font weight for Display1 text |
| `--salt-text-display1-fontWeight-small` | Light font weight for Display1 text |
| `--salt-text-display1-fontWeight-strong` | Bold font weight for Display1 text |
| `--salt-text-display1-fontSize` | Font size for Display1 text (density-dependent) |
| `--salt-text-display1-lineHeight` | Line height for Display1 text (density-dependent) |

#### Display2

| Variable | Description |
|----------|-------------|
| `--salt-text-display2-fontFamily` | Font family for Display2 text |
| `--salt-text-display2-fontWeight` | Regular font weight for Display2 text |
| `--salt-text-display2-fontWeight-small` | Light font weight for Display2 text |
| `--salt-text-display2-fontWeight-strong` | Bold font weight for Display2 text |
| `--salt-text-display2-fontSize` | Font size for Display2 text (density-dependent) |
| `--salt-text-display2-lineHeight` | Line height for Display2 text (density-dependent) |

#### Display3

| Variable | Description |
|----------|-------------|
| `--salt-text-display3-fontFamily` | Font family for Display3 text |
| `--salt-text-display3-fontWeight` | Regular font weight for Display3 text |
| `--salt-text-display3-fontWeight-small` | Light font weight for Display3 text |
| `--salt-text-display3-fontWeight-strong` | Bold font weight for Display3 text |
| `--salt-text-display3-fontSize` | Font size for Display3 text (density-dependent) |
| `--salt-text-display3-lineHeight` | Line height for Display3 text (density-dependent) |

#### Display4

| Variable | Description |
|----------|-------------|
| `--salt-text-display4-fontFamily` | Font family for Display4 text |
| `--salt-text-display4-fontWeight` | Regular font weight for Display4 text |
| `--salt-text-display4-fontWeight-small` | Light font weight for Display4 text |
| `--salt-text-display4-fontWeight-strong` | Bold font weight for Display4 text |
| `--salt-text-display4-fontSize` | Font size for Display4 text (density-dependent) |
| `--salt-text-display4-lineHeight` | Line height for Display4 text (density-dependent) |

### Notation Text

| Variable | Description |
|----------|-------------|
| `--salt-text-notation-fontFamily` | Font family for notation text |
| `--salt-text-notation-fontWeight` | Regular font weight for notation text |
| `--salt-text-notation-fontWeight-small` | Light font weight for notation text |
| `--salt-text-notation-fontWeight-strong` | Bold font weight for notation text |
| `--salt-text-notation-fontSize` | Font size for notation text (density-dependent) |
| `--salt-text-notation-lineHeight` | Line height for notation text (density-dependent) |

### Code Text

| Variable | Description |
|----------|-------------|
| `--salt-text-code-fontFamily` | Font family for code text |

## Font Sizes and Line Heights by Density

### Touch Density (`salt-density-touch`)

| Text Style | Font Size | Line Height |
|------------|-----------|-------------|
| Body | 16px | 20px |
| H1 | 42px | 54px |
| H2 | 32px | 42px |
| H3 | 24px | 32px |
| H4 | 16px | 20px |
| Label | 14px | 18px |
| Display1 | 84px | 109px |
| Display2 | 58px | 76px |
| Display3 | 42px | 54px |
| Display4 | 42px | 54px |
| Notation | 14px | 18px |

### Low Density (`salt-density-low`)

| Text Style | Font Size | Line Height |
|------------|-----------|-------------|
| Body | 14px | 18px |
| H1 | 32px | 42px |
| H2 | 24px | 32px |
| H3 | 18px | 24px |
| H4 | 14px | 18px |
| Label | 12px | 16px |
| Display1 | 68px | 88px |
| Display2 | 46px | 60px |
| Display3 | 32px | 42px |
| Display4 | 32px | 42px |
| Notation | 12px | 16px |

### Medium Density (`salt-density-medium`)

| Text Style | Font Size | Line Height |
|------------|-----------|-------------|
| Body | 12px | 16px |
| H1 | 24px | 32px |
| H2 | 18px | 24px |
| H3 | 14px | 18px |
| H4 | 12px | 16px |
| Label | 11px | 14px |
| Display1 | 54px | 70px |
| Display2 | 36px | 47px |
| Display3 | 24px | 32px |
| Display4 | 24px | 32px |
| Notation | 10px | 13px |

### High Density (`salt-density-high`)

| Text Style | Font Size | Line Height |
|------------|-----------|-------------|
| Body | 11px | 14px |
| H1 | 18px | 24px |
| H2 | 14px | 18px |
| H3 | 12px | 16px |
| H4 | 11px | 14px |
| Label | 10px | 13px |
| Display1 | 42px | 54px |
| Display2 | 28px | 36px |
| Display3 | 18px | 24px |
| Display4 | 18px | 24px |
| Notation | 8px | 10px |

## Usage Examples

### Basic Text Styling

```css
.body-text {
  font-family: var(--salt-text-fontFamily);
  font-weight: var(--salt-text-fontWeight);
  font-size: var(--salt-text-fontSize);
  line-height: var(--salt-text-lineHeight);
}

.heading {
  font-family: var(--salt-text-h2-fontFamily);
  font-weight: var(--salt-text-h2-fontWeight);
  font-size: var(--salt-text-h2-fontSize);
  line-height: var(--salt-text-h2-lineHeight);
}

.field-label {
  font-family: var(--salt-text-label-fontFamily);
  font-weight: var(--salt-text-label-fontWeight);
  font-size: var(--salt-text-label-fontSize);
  line-height: var(--salt-text-label-lineHeight);
}
```

### Creating Button Text

```css
.button-text {
  font-family: var(--salt-text-action-fontFamily);
  font-weight: var(--salt-text-action-fontWeight);
  letter-spacing: var(--salt-text-action-letterSpacing);
  text-transform: var(--salt-text-action-textTransform);
  text-align: var(--salt-text-action-textAlign);
}
```

### Creating Display Text

```css
.hero-title {
  font-family: var(--salt-text-display1-fontFamily);
  font-weight: var(--salt-text-display1-fontWeight);
  font-size: var(--salt-text-display1-fontSize);
  line-height: var(--salt-text-display1-lineHeight);
}
```

### Creating Code Snippets

```css
.code-example {
  font-family: var(--salt-text-code-fontFamily);
  font-size: var(--salt-text-fontSize);
  line-height: var(--salt-text-lineHeight);
}
```

## Best Practices

1. Use the appropriate text category based on the content's purpose (body, heading, label, etc.)
2. Respect the typographic hierarchy to maintain visual organization
3. Maintain consistent font usage throughout your application
4. Consider density settings based on your target devices:
   - Touch density for touchscreen and tablet interfaces
   - Low density for casual desktop applications
   - Medium density for professional desktop applications
   - High density for information-dense applications
5. Use font weight variants consistently:
   - Small/light weights for less emphasis
   - Regular weights for standard text
   - Strong/bold weights for emphasis 