- **Property:** break-after
- **Shorthand:** brka  
  Utilities for controlling how a column or page should break after an element.

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
brkaAll {
  break-after: all;
}
brkaPage {
  break-after: page;
}
brkaLeft {
  break-after: left;
}
brkaRight {
  break-after: right;
}
brkaRecto {
  break-after: recto;
}
brkaVerso {
  break-after: verso;
}
brkaColumn {
  break-after: column;
}
brkaAvoidPage {
  break-after: avoid-page;
}
brkaAvoidColumn {
  break-after: avoid-column;
}
brkaAvoidRegion {
  break-after: avoid-region;
}
```

The `break-after` property controls how page, column, or region breaks should behave after an element. This is particularly useful for print layouts, paginated content, and multi-column layouts.

## Usage Examples

### Default Behavior with brkaAuto

```html
<div class="example-container">
  <p class="brkaAuto">
    This paragraph uses the default break behavior. The browser will determine
    if a break should occur after this element.
  </p>
  <p>
    The browser decides whether to insert a break after the previous element.
  </p>
</div>
```

With `brkaAuto`, the browser automatically determines whether to insert a break after the element based on available space and other layout considerations.

### Preventing Breaks with brkaAvoid

```html
<div class="example-container">
  <h3>Section Title</h3>
  <p class="brkaAvoid">
    This paragraph has brkaAvoid applied. The browser will try to avoid breaking
    after this paragraph, keeping it together with the content that follows.
  </p>
  <p>This paragraph should ideally stay with the previous paragraph.</p>
</div>
```

The `brkaAvoid` class tells the browser to avoid inserting a page or column break after the element if possible.

### Forcing Page Breaks with brkaAlways

```html
<div class="example-container">
  <h3>Chapter 1</h3>
  <p>This is the end of Chapter 1.</p>
  <p class="brkaAlways">
    This paragraph forces a page break after it. The next content will start on
    a new page.
  </p>
  <h3>Chapter 2</h3>
  <p>This content appears on a new page.</p>
</div>
```

The `brkaAlways` class forces a page break after the element, ensuring the following content starts on a new page.

### Page Break with brkaPage

```html
<div class="example-container">
  <p>This is the end of the current page.</p>
  <p class="brkaPage">
    This paragraph forces a page break after it, similar to brkaAlways but
    specifically for paged media.
  </p>
  <p>This content appears on a new page.</p>
</div>
```

The `brkaPage` class is similar to `brkaAlways` but is specifically designed for paged media contexts.

### Column Breaks with brkaColumn

```html
<div class="col2 gap40px">
  <p>This is the first part of content in a multi-column layout.</p>
  <p class="brkaColumn">
    This paragraph forces a column break. The next content will start in a new
    column.
  </p>
  <p>
    This content appears at the top of the next column due to the column break.
  </p>
  <p>Additional content continues flowing in the second column.</p>
</div>
```

In multi-column layouts, `brkaColumn` forces the content after the element to begin in a new column.

### Page Position Control with brkaLeft and brkaRight

```html
<div class="example-container print-example">
  <p>Content on the initial page.</p>
  <p class="brkaLeft">
    This paragraph forces a page break, and the next content will appear on a
    left page in a spread.
  </p>
  <p>This content appears on a left page.</p>
  <p class="brkaRight">
    This paragraph forces a page break, and the next content will appear on a
    right page in a spread.
  </p>
  <p>This content appears on a right page.</p>
</div>
```

The `brkaLeft` and `brkaRight` classes are useful for controlling content positioning in book-like layouts with facing pages.

### Recto and Verso Page Control

```html
<div class="example-container print-example">
  <p>Content on the initial page.</p>
  <p class="brkaRecto">
    This paragraph forces a page break, and the next content will appear on a
    recto (right-hand) page.
  </p>
  <p>This content appears on a recto (right-hand) page.</p>
  <p class="brkaVerso">
    This paragraph forces a page break, and the next content will appear on a
    verso (left-hand) page.
  </p>
  <p>This content appears on a verso (left-hand) page.</p>
</div>
```

The `brkaRecto` and `brkaVerso` classes provide alternative ways to control page positioning in book layouts.

### Specific Avoidance with brkaAvoidPage, brkaAvoidColumn, and brkaAvoidRegion

```html
<div class="example-container">
  <p class="brkaAvoidPage">
    This paragraph prevents a page break after it, but may allow column breaks.
  </p>
  <p>This content should stay on the same page as the previous paragraph.</p>
</div>

<div class="example-container">
  <div class="col3 gap20px">
    <p>First column content.</p>
    <p class="brkaAvoidColumn">
      This paragraph prevents a column break after it, but may allow page
      breaks.
    </p>
    <p>
      This content should stay in the same column as the previous paragraph.
    </p>
    <p>More content that continues in the columns.</p>
  </div>
</div>
```

These specialized avoidance classes provide more granular control over different types of breaks.
