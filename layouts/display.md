- **Property:** display
- **Shorthand:** d
  Utilities for controlling the display type of an element.

```css
dB {
  display: block;
}
dI {
  display: inline;
}
dIb {
  display: inline-block;
}
dF {
  display: flex;
}
dIf {
  display: inline-flex;
}
dG {
  display: grid;
}
dIg {
  display: inline-grid;
}
dFr {
  display: flow-root;
}
dT {
  display: table;
}
dIt {
  display: inline-table;
}
dTr {
  display: table-row;
}
dTcell {
  display: table-cell;
}
dTcp {
  display: table-caption;
}
dTcol {
  display: table-column;
}
dTcolg {
  display: table-column-group;
}
dThg {
  display: table-header-group;
}
dTrg {
  display: table-row-group;
}
dTfg {
  display: table-footer-group;
}
dC {
  display: contents;
}
dLi {
  display: list-item;
}
dN {
  display: none;
}
```

The `display` property controls how an element is displayed and how it participates in layout. This is fundamental for creating layouts and controlling element behavior.

## Text Flow Display Types

**Example:**

```html
<p>
  When controlling the flow of text, using the CSS property
  <span class="dI">display: inline</span> will cause the text inside the element
  to wrap normally.
</p>
<p>
  While using the property
  <span class="dIb">display: inline-block will wrap the element</span> to
  prevent the text inside from extending beyond its parent.
</p>
<p>
  Lastly, using the property <span class="dB">display: block</span> will put the
  element on its own line and fill its parent.
</p>
```

![Text flow display example](./img/display/text-flow.png)

## Flex Display

```css
dF {
  display: flex;
}
```

**Example:**

```html
<div class="dF gap20px p20px bgcLightGray bd1px;solid;#333">
  <div>Flex Item 1</div>
  <div>Flex Item 2</div>
  <div>Flex Item 3</div>
</div>
```

![Flex display example](./img/display/flex.png)

## Grid Display

```css
dG {
  display: grid;
}
```

**Example:**

```html
<div class="dG gtc1fr;1fr gap20px p20px bgcLightGray bd1px;solid;#333">
  <div>Grid Item 1</div>
  <div>Grid Item 2</div>
  <div>Grid Item 3</div>
  <div>Grid Item 4</div>
</div>
```

![Grid display example](./img/display/grid.png)

## Inline Flex Display

```css
dIf {
  display: inline-flex;
}
```

**Example:**

```html
<p>
  This is inline text with an
  <span class="dIf gap10px p10px bgcLightGray bd1px;solid;#333">
    <span>Item 1</span>
    <span>Item 2</span>
  </span>
  inline flex container that flows with the text.
</p>
```

![Inline flex display example](./img/display/inline-flex.png)

## Inline Grid Display

```css
dIg {
  display: inline-grid;
}
```

**Example:**

```html
<p>
  This is inline text with an
  <span class="dIg gtc1fr;1fr gap5px p10px bgcLightGray bd1px;solid;#333">
    <span>A</span>
    <span>B</span>
    <span>C</span>
    <span>D</span>
  </span>
  inline grid container that flows with the text.
</p>
```

![Inline grid display example](./img/display/inline-grid.png)

## Flow Root Display

```css
dFr {
  display: flow-root;
}
```

The `flow-root` display value creates a new block formatting context, which is useful for containing floated elements and preventing margin collapse. It's particularly helpful when you need to clear floats without using additional markup.

**Example:**

```html
<div class="dFr p20px bgcLightGray bd1px;solid;#333">
  <div class="flL">Floated element</div>
  <p>
    Flow-root creates a new block formatting context that contains floated
    elements and prevents them from escaping their container.
  </p>
</div>
```

![Flow root display example](./img/display/flow-root.png)

## Table Display

```css
dT {
  display: table;
}
dIt {
  display: inline-table;
}
dTr {
  display: table-row;
}
dTcell {
  display: table-cell;
}
dTcp {
  display: table-caption;
}
dTcol {
  display: table-column;
}
dTcolg {
  display: table-column-group;
}
dThg {
  display: table-header-group;
}
dTrg {
  display: table-row-group;
}
dTfg {
  display: table-footer-group;
}
```

The table display utilities allow you to create table-like layouts using CSS display properties. This is useful when you need table semantics without using actual HTML table elements, or when you want to apply table layout to non-table elements.

**Basic Table Example:**

```html
<div class="dT">
  <div class="dTr">
    <div class="dTcell">Cell 1</div>
    <div class="dTcell">Cell 2</div>
  </div>
  <div class="dTr">
    <div class="dTcell">Cell 3</div>
    <div class="dTcell">Cell 4</div>
  </div>
</div>
```

**Complete Table Structure Example:**

```html
<div class="dT">
  <div class="dTcp">Table Caption</div>
  <div class="dThg">
    <div class="dTr">
      <div class="dTcell">Header 1</div>
      <div class="dTcell">Header 2</div>
    </div>
  </div>
  <div class="dTrg">
    <div class="dTr">
      <div class="dTcell">Data 1</div>
      <div class="dTcell">Data 2</div>
    </div>
  </div>
  <div class="dTfg">
    <div class="dTr">
      <div class="dTcell">Footer 1</div>
      <div class="dTcell">Footer 2</div>
    </div>
  </div>
</div>
```

![Complete table display example](./img/display/table-complete.png)

## Contents Display

```css
dC {
  display: contents;
}
```

The `contents` display value makes the element's children appear as if they were direct children of the element's parent, effectively removing the element from the layout tree while keeping its children.

**Example:**

```html
<div class="dF">
  <div>Item 1</div>
  <div class="dC">
    <div>Item 2 (in contents wrapper)</div>
    <div>Item 3 (in contents wrapper)</div>
  </div>
  <div>Item 4</div>
</div>
```

![Contents display example](./img/display/contents.png)

## List Item Display

```css
dLi {
  display: list-item;
}
```

The `list-item` display value makes any element behave like a list item, including generating a marker box (bullet point or number).

**Example:**

```html
<div>
  <div class="dLi">This div behaves like a list item</div>
  <div class="dLi">Another list item div</div>
  <div class="dLi">Third list item div</div>
</div>
```

![List item display example](./img/display/list-item.png)

## None Display

```css
dN {
  display: none;
}
```

**Example:**

```html
<div>Visible element</div>
<div class="dN">Hidden element</div>
<div>Another visible element</div>
```

![None display example](./img/display/none.png)
