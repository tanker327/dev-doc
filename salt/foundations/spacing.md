# Salt Design System - Spacing Guidelines

## Spacing Variables

The Salt Design System provides a comprehensive set of spacing variables that scale based on density settings. All spacing values are derived from a base unit (`--salt-spacing-100`) which changes according to the selected density.

### Base Spacing by Density

| Density | Base Value (`--salt-spacing-100`) |
|---------|-----------------------------------|
| Touch   | 16px                              |
| Low     | 12px                              |
| Medium  | 8px                               |
| High    | 4px                               |

### Available Spacing Variables

All spacing variables are calculated as multiples of the base spacing value. The following spacing tokens are available:

| Variable              | Calculation                           | Touch (16px) | Low (12px) | Medium (8px) | High (4px) |
|-----------------------|--------------------------------------|--------------|------------|--------------|------------|
| `--salt-spacing-25`   | 0.25 × `--salt-spacing-100`          | 4px          | 3px        | 2px          | 1px        |
| `--salt-spacing-50`   | 0.5 × `--salt-spacing-100`           | 8px          | 6px        | 4px          | 2px        |
| `--salt-spacing-75`   | 0.75 × `--salt-spacing-100`          | 12px         | 9px        | 6px          | 3px        |
| `--salt-spacing-100`  | Base unit                            | 16px         | 12px       | 8px          | 4px        |
| `--salt-spacing-150`  | 1.5 × `--salt-spacing-100`           | 24px         | 18px       | 12px         | 6px        |
| `--salt-spacing-200`  | 2 × `--salt-spacing-100`             | 32px         | 24px       | 16px         | 8px        |
| `--salt-spacing-250`  | 2.5 × `--salt-spacing-100`           | 40px         | 30px       | 20px         | 10px       |
| `--salt-spacing-300`  | 3 × `--salt-spacing-100`             | 48px         | 36px       | 24px         | 12px       |
| `--salt-spacing-350`  | 3.5 × `--salt-spacing-100`           | 56px         | 42px       | 28px         | 14px       |
| `--salt-spacing-400`  | 4 × `--salt-spacing-100`             | 64px         | 48px       | 32px         | 16px       |
| `--salt-spacing-450`  | 4.5 × `--salt-spacing-100`           | 72px         | 54px       | 36px         | 18px       |
| `--salt-spacing-500`  | 5 × `--salt-spacing-100`             | 80px         | 60px       | 40px         | 20px       |
| `--salt-spacing-550`  | 5.5 × `--salt-spacing-100`           | 88px         | 66px       | 44px         | 22px       |
| `--salt-spacing-600`  | 6 × `--salt-spacing-100`             | 96px         | 72px       | 48px         | 24px       |
| `--salt-spacing-650`  | 6.5 × `--salt-spacing-100`           | 104px        | 78px       | 52px         | 26px       |
| `--salt-spacing-700`  | 7 × `--salt-spacing-100`             | 112px        | 84px       | 56px         | 28px       |
| `--salt-spacing-750`  | 7.5 × `--salt-spacing-100`           | 120px        | 90px       | 60px         | 30px       |
| `--salt-spacing-800`  | 8 × `--salt-spacing-100`             | 128px        | 96px       | 64px         | 32px       |
| `--salt-spacing-850`  | 8.5 × `--salt-spacing-100`           | 136px        | 102px      | 68px         | 34px       |
| `--salt-spacing-900`  | 9 × `--salt-spacing-100`             | 144px        | 108px      | 72px         | 36px       |
| `--salt-spacing-950`  | 9.5 × `--salt-spacing-100`           | 152px        | 114px      | 76px         | 38px       |

## Usage

### CSS Usage

```css
.my-component {
  padding: var(--salt-spacing-100);
  margin-bottom: var(--salt-spacing-200);
  gap: var(--salt-spacing-50);
}
```

### Best Practices

1. Always use spacing variables instead of hardcoded pixel values
2. Choose the appropriate token based on the UI element's context and density requirements
3. For responsive layouts, consider how spacing will scale across different densities

## Density Classes

To apply a specific density to a component or container, use one of the following CSS classes:

- `.salt-density-touch` - For touch interfaces (16px base)
- `.salt-density-low` - For lower density interfaces (12px base)
- `.salt-density-medium` - For medium density interfaces (8px base)
- `.salt-density-high` - For high density interfaces (4px base)

Example:
```html
<div class="salt-density-medium">
  <!-- Components inside this container will use medium density spacing -->
</div>
```
