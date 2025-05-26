# Installation

This guide explains how to install and set up the utility CSS framework in your project.

## Quick Start

### CDN Installation

Add the following script to the end of your HTML body:

```html
<script type="module">
  import $ from "https://unpkg.com/fwkuijs@1.0.3/fw.js";
  window.$ = $;
  $.start();
  // Your custom code here
</script>
```

### Local Installation

1. Download the framework and place it in your assets directory
2. Add the following script to the end of your HTML body:

```html
<script type="module">
  import $ from "/assets/fw.js";
  window.$ = $;
  $.start();
  // Your custom code here
</script>
```

## CSS Class Syntax

The framework uses a consistent syntax for generating utility classes:

```
[<MQ>:][<layer>]<pvCSS>[<selector>]
```

Where:

- `[<MQ>]`: Optional media query prefix (xs, sm, md, lg, xl, 2xl)
- `[<layer>]`: Optional layer number (1-19) for specificity control
- `<pvCSS>`: Required property-value combination
- `[<selector>]`: Optional CSS selector

> **Note:** See [Documentation Conventions](./conventions.md) for detailed explanation of placeholders.

## Special Characters

| Character | Purpose                       | Example              |
| --------- | ----------------------------- | -------------------- |
| `&`       | Combines properties           | `cRed&bgcGreen`      |
| `;`       | Replaces spaces in values     | `calc(100vw;-;10px)` |
| `@`       | Separates selector from class | `cRed@:hover`        |
| `!`       | Adds importance to property   | `c!red`              |

## Media Query Breakpoints

| Prefix | Media Query       |
| ------ | ----------------- |
| `xs:`  | max-width: 575px  |
| `sm:`  | min-width: 576px  |
| `md:`  | min-width: 768px  |
| `lg:`  | min-width: 992px  |
| `xl:`  | min-width: 1200px |
| `2xl:` | min-width: 1400px |

## Layer System

Layers control specificity with values from 1-19 (higher numbers have greater specificity):

```css
@layer l0,l1,l2,...l19;
```

Example: `1c#000` applies color in layer 1.

## Property-Value Syntax

The core of each utility class follows this structure:

```
<pCSS>[!]<vCSS>
```

Where:

- `<pCSS>`: Property shorthand or full property name
- `[!]`: Optional importance marker
- `<vCSS>`: Value in one of these formats:
  - `#123456`: Hex color codes
  - `--variable-name`: CSS variables
  - `{value}`: Values in curly braces
  - `Capitalized`: Values with first letter capitalized
  - Numeric values: `10px`, `.5rem`, etc.

## Usage Examples

### Basic Property-Value

```html
<div class="cRed">Red text</div>
<div class="bgc#f5f5f5">Gray background</div>
```

### Responsive Design

```html
<div class="xs:cRed md:cBlue">Red on mobile, blue on medium screens and up</div>
```

### Combined Properties

```html
<div class="cRed&bgcGreen">Red text on green background</div>
```

### With Selectors

```html
<button class="cBlue@:hover">Blue on hover</button>
```

### With Layers

```html
<div class="1cRed 2cBlue">Blue text (layer 2 overrides layer 1)</div>
```

## Next Steps

- See [Usage Guide](./usage.md) for more detailed examples
