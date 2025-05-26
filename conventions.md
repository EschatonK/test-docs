# Documentation Conventions

This guide explains the syntax and placeholders used throughout our utility class documentation.

## Code Syntax Placeholders

When browsing our documentation, you'll encounter placeholders in code examples that represent variable parts of CSS properties and values:

| Placeholder  | Meaning                   | Example Usage                                                   |
| ------------ | ------------------------- | --------------------------------------------------------------- |
| `pCSS`       | CSS Property              | `pCSS: value;` represents a CSS property like `display: value;` |
| `vCSS`       | CSS Value                 | `property: vCSS;` represents a CSS value like `property: flex;` |
| `brka<vCSS>` | Class with variable value | Represents classes like `brkaAuto`, `brkaAvoid`, etc.           |

## Example Interpretation

When you see code like:

```css
brka<vCSS > {
  break-after: <vCSS>;
}
```

This means there are multiple utility classes following this pattern, where `<vCSS>` is replaced with specific values:

```css
brkaAuto {
  break-after: auto;
}
brkaAvoid {
  break-after: avoid;
}
brkaAlways {
  break-after: always;
}
```
