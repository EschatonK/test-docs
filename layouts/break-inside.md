- **Property:** break-inside
- **Shorthand:** brki  
  Utilities for controlling how a column or page break should behave inside an element.

```css
brkiAuto {
  break-inside: auto;
}
brkiAvoid {
  break-inside: avoid;
}
brkiAvoidPage {
  break-inside: avoid-page;
}
brkiAvoidColumn {
  break-inside: avoid-column;
}
brkiAvoidRegion {
  break-inside: avoid-region;
}
```

The `break-inside` property controls how page, column, or region breaks should behave inside an element. This is particularly useful for preventing content from being split across pages or columns in print layouts and multi-column layouts.

## Usage Examples

### Default Behavior with brkiAuto

```html
<div class="example-container">
  <div class="col2 gap40px">
    <div class="brkiAuto">
      <h3>Section Title</h3>
      <p>
        This container uses the default break behavior. The browser will
        determine if breaks should occur within this element based on available
        space and layout needs.
      </p>
      <p>
        Additional content may be split across columns or pages as the browser
        deems necessary.
      </p>
    </div>
  </div>
</div>
```

With `brkiAuto`, the browser automatically determines whether to insert breaks within the element based on available space and other layout considerations. Content may be split across columns or pages.

### Preventing All Breaks with brkiAvoid

```html
<div class="example-container">
  <div class="col2 gap40px">
    <div class="brkiAvoid">
      <h3>Important Notice</h3>
      <p>
        This container has brkiAvoid applied. The browser will try to avoid
        breaking within this element, keeping all its content together in the
        same column or page.
      </p>
      <p>
        This is useful for content that should be read as a cohesive unit, such
        as notices, warnings, or short sections that lose meaning when split.
      </p>
    </div>
    <p>Other content can flow normally around the avoided break element.</p>
  </div>
</div>
```

The `brkiAvoid` class tells the browser to avoid inserting any type of break (page, column, or region) within the element if possible. This keeps the entire content block together.

### Preventing Page Breaks with brkiAvoidPage

```html
<div class="example-container print-example">
  <div class="brkiAvoidPage">
    <h3>Table of Contents</h3>
    <ul>
      <li>Chapter 1: Introduction</li>
      <li>Chapter 2: Main Concepts</li>
      <li>Chapter 3: Advanced Techniques</li>
      <li>Chapter 4: Case Studies</li>
      <li>Chapter 5: Conclusion</li>
    </ul>
  </div>
  <p>
    The table of contents above will try to stay on the same page, but may be
    split across columns if necessary.
  </p>
</div>
```

The `brkiAvoidPage` class prevents page breaks within the element but allows column breaks. This is useful for content that should remain on the same page but can be split across columns.

### Preventing Column Breaks with brkiAvoidColumn

```html
<div class="example-container">
  <div class="col3 gap20px">
    <figure class="brkiAvoidColumn">
      <div class="bgcGray p20px">Image placeholder</div>
      <figcaption>
        This figure and its caption will stay in the same column, but may be
        moved to a new page if necessary.
      </figcaption>
    </figure>
    <p>
      The figure above uses brkiAvoidColumn to ensure the image and its caption
      stay together in the same column.
    </p>
    <p>
      This is particularly useful for figures, tables, code blocks, and other
      content that should not be split across columns.
    </p>
  </div>
</div>
```

In multi-column layouts, `brkiAvoidColumn` prevents column breaks within the element but allows page breaks. This ensures related content like figures and their captions stay together in the same column.

### Preventing Region Breaks with brkiAvoidRegion

```html
<div class="example-container">
  <div class="brkiAvoidRegion">
    <h3>Special Feature</h3>
    <p>
      This content uses brkiAvoidRegion to prevent region breaks within it. This
      is relevant in CSS Regions, where content flows through multiple defined
      regions.
    </p>
    <p>The entire feature will try to stay within the same region.</p>
  </div>
</div>
```

The `brkiAvoidRegion` class prevents region breaks within the element. This is primarily useful in CSS Regions contexts, where content flows through multiple defined regions.

## Practical Applications

### Card Components

```html
<div class="example-container">
  <div class="col3 gap20px">
    <div class="brkiAvoid p15px brd1px brdcGray">
      <h4>Card Title</h4>
      <p>
        This card uses brkiAvoid to ensure all its content stays together in the
        same column and page.
      </p>
      <button class="p5px;10px bgcBlue cWhite">Read More</button>
    </div>
    <div class="brkiAvoid p15px brd1px brdcGray">
      <h4>Another Card</h4>
      <p>
        Cards with brkiAvoid maintain their visual integrity in multi-column
        layouts and when printed.
      </p>
      <button class="p5px;10px bgcBlue cWhite">Read More</button>
    </div>
    <p>
      Additional content can flow around the cards, potentially breaking across
      columns or pages as needed.
    </p>
  </div>
</div>
```

Using `brkiAvoid` on card components ensures they maintain their visual integrity in multi-column layouts and when printed.

### Tables and Data Presentation

```html
<div class="example-container">
  <div class="col2 gap40px">
    <table class="brkiAvoid w100% brd1px brdcGray">
      <thead>
        <tr>
          <th class="p10px brdcGray brd1px">Name</th>
          <th class="p10px brdcGray brd1px">Value</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="p10px brdcGray brd1px">Item 1</td>
          <td class="p10px brdcGray brd1px">$100</td>
        </tr>
        <tr>
          <td class="p10px brdcGray brd1px">Item 2</td>
          <td class="p10px brdcGray brd1px">$200</td>
        </tr>
        <tr>
          <td class="p10px brdcGray brd1px">Item 3</td>
          <td class="p10px brdcGray brd1px">$300</td>
        </tr>
      </tbody>
    </table>
    <p>
      The table above uses brkiAvoid to ensure it doesn't get split across
      columns or pages, maintaining data integrity and readability.
    </p>
  </div>
</div>
```

Tables with `brkiAvoid` maintain their structure and readability by preventing breaks within the table.
