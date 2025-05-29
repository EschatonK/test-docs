- **Property:** break-before
- **Shorthand:** brkb  
  Utilities for controlling how a column or page should break before an element.

```css
brkbAuto {
  break-before: auto;
}
brkbAvoid {
  break-before: avoid;
}
brkbAlways {
  break-before: always;
}
brkbAll {
  break-before: all;
}
brkbPage {
  break-before: page;
}
brkbLeft {
  break-before: left;
}
brkbRight {
  break-before: right;
}
brkbRecto {
  break-before: recto;
}
brkbVerso {
  break-before: verso;
}
brkbColumn {
  break-before: column;
}
brkbAvoidPage {
  break-before: avoid-page;
}
brkbAvoidColumn {
  break-before: avoid-column;
}
brkbAvoidRegion {
  break-before: avoid-region;
}
```

The `break-before` property controls how page, column, or region breaks should behave before an element. This is particularly useful for print layouts, paginated content, and multi-column layouts.

## Usage Examples

### Default Behavior with brkbAuto

```html
<div class="example-container">
  <p>This paragraph comes before the element with break-before applied.</p>
  <p class="brkbAuto">
    This paragraph uses the default break behavior. The browser will determine
    if a break should occur before this element.
  </p>
</div>
```

With `brkbAuto`, the browser automatically determines whether to insert a break before the element based on available space and other layout considerations.

### Preventing Breaks with brkbAvoid

```html
<div class="example-container">
  <p>This paragraph comes before the heading and should stay with it.</p>
  <h3 class="brkbAvoid">Section Title</h3>
  <p>
    This heading has brkbAvoid applied. The browser will try to avoid breaking
    before this heading, keeping it together with the content that precedes it.
  </p>
</div>
```

The `brkbAvoid` class tells the browser to avoid inserting a page or column break before the element if possible.

### Forcing Page Breaks with brkbAlways

```html
<div class="example-container">
  <h3>Chapter 1</h3>
  <p>This is the content of Chapter 1.</p>
  <h3 class="brkbAlways">Chapter 2</h3>
  <p>
    This heading forces a page break before it. This content appears on a new
    page, starting with the Chapter 2 heading.
  </p>
</div>
```

The `brkbAlways` class forces a page break before the element, ensuring the element starts on a new page.

### Page Break with brkbPage

```html
<div class="example-container">
  <p>This is content on the current page.</p>
  <h2 class="brkbPage">New Section</h2>
  <p>
    This heading forces a page break before it, similar to brkbAlways but
    specifically for paged media.
  </p>
</div>
```

The `brkbPage` class is similar to `brkbAlways` but is specifically designed for paged media contexts.

### Column Breaks with brkbColumn

```html
<div class="example-container">
  <div class="col2 gap40px">
    <p>This is the first part of content in a multi-column layout.</p>
    <p>More content in the first column.</p>
    <h4 class="brkbColumn">
      This heading forces a column break before it. It will appear at the top of
      a new column.
    </h4>
    <p>
      This content appears in the second column along with the heading above.
    </p>
    <p>Additional content continues flowing in the second column.</p>
  </div>
</div>
```

In multi-column layouts, `brkbColumn` forces the element and content after it to begin in a new column.

### Page Position Control with brkbLeft and brkbRight

```html
<div class="example-container print-example">
  <p>Content on the initial page.</p>
  <h2 class="brkbLeft">Left Page Section</h2>
  <p>
    This heading forces a page break before it, and it will appear on a left
    page in a spread.
  </p>
  <h2 class="brkbRight">Right Page Section</h2>
  <p>
    This heading forces a page break before it, and it will appear on a right
    page in a spread.
  </p>
</div>
```

The `brkbLeft` and `brkbRight` classes are useful for controlling content positioning in book-like layouts with facing pages.

### Recto and Verso Page Control

```html
<div class="example-container print-example">
  <p>Content on the initial page.</p>
  <h2 class="brkbRecto">Recto Page Section</h2>
  <p>
    This heading forces a page break before it, and it will appear on a recto
    (right-hand) page.
  </p>
  <h2 class="brkbVerso">Verso Page Section</h2>
  <p>
    This heading forces a page break before it, and it will appear on a verso
    (left-hand) page.
  </p>
</div>
```

The `brkbRecto` and `brkbVerso` classes provide alternative ways to control page positioning in book layouts.

### Specific Avoidance with brkbAvoidPage, brkbAvoidColumn, and brkbAvoidRegion

```html
<div class="example-container">
  <p>This is content on the current page.</p>
  <h3 class="brkbAvoidPage">
    This heading prevents a page break before it, but may allow column breaks.
  </h3>
  <p>This heading should stay on the same page as the previous content.</p>
</div>

<div class="col3 gap20px">
  <p>First column content.</p>
  <p>More content in the first column.</p>
  <h4 class="brkbAvoidColumn">
    This heading prevents a column break before it, but may allow page breaks.
  </h4>
  <p>This heading should stay in the same column as the previous content.</p>
  <p>More content that continues in the columns.</p>
</div>
```

These specialized avoidance classes provide more granular control over different types of breaks.

### All Breaks with brkbAll

```html
<div class="example-container">
  <p>This is content before the break.</p>
  <h2 class="brkbAll">
    This heading forces the strongest possible break before it. In paged media,
    this creates a page break. In multi-column layouts, it forces a column
    break.
  </h2>
  <p>
    This content appears after the strongest possible break with the heading.
  </p>
</div>
```

The `brkbAll` class creates the strongest possible break before the element. It's a more forceful version that ensures breaks occur in all contexts where breaks are possible.
