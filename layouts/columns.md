- **Property:** columns
- **Shorthand:** col
  Utilities for controlling CSS multi-column layout properties.

```css
colA {
  columns: auto;
}
```

The `columns` property creates multi-column layouts. Use column utilities to control count, width, spacing, rules, and content flow.

## Column Count

```css
colc<vCSS > {
  column-count: <vCSS>;
}
```

**Example:**

```html
<div class="colc3">
  <p>
    Content automatically divided into 3 columns. Lorem ipsum dolor sit amet,
    consectetur adipiscing elit.
  </p>
  <p>
    Additional content flows naturally across the columns with automatic height
    balancing.
  </p>
</div>
```

![Column count example](./img/columns/colc3.png)

## Column Width

```css
colw<vCSS > {
  column-width: <vCSS>;
}
```

**Example:**

```html
<div class="colw200px">
  <p>
    Creates columns approximately 200px wide. Browser determines column count
    based on container width.
  </p>
</div>
```

![Column width example](./img/columns/colw200px.png)

## Column Gap

```css
colg<vCSS > {
  column-gap: <vCSS>;
}
```

**Example:**

```html
<div class="colc2 colg50px">
  <p>Two-column layout with 50px spacing between columns.</p>
  <p>Two-column layout with 50px spacing between columns.</p>
</div>
```

![Column gap example](./img/columns/colg50px.png)

## Column Rule

```css
colr<vCSS > {
  column-rule: <vCSS>;
}
colrw<vCSS > {
  column-rule-width: <vCSS>;
}
colrs<vCSS > {
  column-rule-style: <vCSS>;
}
colrc<vCSS > {
  column-rule-color: <vCSS>;
}
```

**Example:**

```html
<div class="colc2 colr1px;solid;#ccc">
  <p>Columns with a 1px solid gray rule between them.</p>
</div>
```

![Column rule example](./img/columns/column-rule.png)

## Column Span

```css
cols<vCSS > {
  column-span: <vCSS>;
}
```

**Example:**

```html
<div class="colc3">
  <h2 class="colsAll">This heading spans all columns</h2>
  <p>This content flows in the normal column layout.</p>
</div>
```

![Column span example](./img/columns/colsAll.png)

## Column Fill

```css
colf<vCSS > {
  column-fill: <vCSS>;
}
```

**Example:**

```html
<div class="colc3 colfAuto">
  <p>Content fills columns sequentially rather than balancing height.</p>
</div>
```

![Column fill example](./img/columns/colfAuto.png)

## Responsive Columns

**Example:**

```html
<div class="xs:colc1 sm:colc2 lg:colc1">
  <div>Card 1</div>
  <div>Card 2</div>
  <div>Card 3</div>
</div>
```

![Responsive columns example](./img/columns/responsive.png)
