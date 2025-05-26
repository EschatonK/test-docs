# Usage Guide

This guide demonstrates how to effectively use the utility CSS framework in your projects with practical examples.

## Basic Usage

### Typography

```html
<h1 class="cBlue fw700 fz24px">Blue Heading with Bold Text</h1>
<p class="cGray lh1.5 fz16px">Gray paragraph with comfortable line height</p>
<span class="ttrU c#333">UPPERCASE TEXT IN DARK GRAY</span>
```

This example shows:
- Text colors with `c` prefix (`cBlue`, `cGray`, `c#333`)
- Font weight with `fw` prefix (`fw700`)
- Font size with `fz` prefix (`fz24px`, `fz16px`)
- Line height with `lh` prefix (`lh1.5`)
- Text transform with `ttr` prefix (`ttrU` for uppercase)

### Display & Visibility

```html
<div class="dF">Flex container</div>
<div class="dG">Grid container</div>
<div class="dB">Block element</div>
<div class="dN">This is hidden</div>
<div class="vH">Invisible but takes up space</div>
```

This example shows:
- Display properties with `d` prefix (`dF` for flex, `dG` for grid, `dB` for block, `dN` for none)
- Visibility control with `v` prefix (`vH` for hidden)

### Spacing

```html
<div class="m10px p20px">Margin 10px, Padding 20px</div>
<div class="mT15px mB15px pX30px">Top/Bottom margins, Left/Right padding</div>
<div class="mx20px my10px">Horizontal margins, Vertical margins</div>
```

This example shows:
- Margin with `m` prefix (`m10px` for all sides)
- Padding with `p` prefix (`p20px` for all sides)
- Directional margins (`mT15px` for top, `mB15px` for bottom)
- Directional padding (`pX30px` for left and right)
- Shorthand for horizontal/vertical spacing (`mx20px`, `my10px`)

## Layout Techniques

### Flexbox Layout

```html
<div class="dF fxdRow fxwW jcSb aiC gap20px">
  <div class="fxg1">Flex item 1</div>
  <div class="fxg2">Flex item 2 (grows more)</div>
  <div class="fxg1">Flex item 3</div>
</div>
```

This creates a flex container with:
- Row direction (`fxdRow`)
- Wrapping enabled (`fxwW`)
- Space-between justification (`jcSb`)
- Center alignment (`aiC`)
- 20px gap between items (`gap20px`)
- Different growth factors for items (`fxg1`, `fxg2`)

### Grid Layout

```html
<div class="dG gtc1fr;2fr;1fr gap15px">
  <div class="gc1/3">Spans 2 columns</div>
  <div>Regular grid item</div>
  <div>Regular grid item</div>
  <div class="grF">Full-width row</div>
</div>
```

This creates a grid with:
- Three columns with different widths (`gtc1fr;2fr;1fr`)
- 15px gaps between items (`gap15px`)
- An item spanning 2 columns (`gc1/3`)
- A full-width row at the bottom (`grF`)

## Common UI Components

### Card Component

```html
<div class="dF fxdColumn p20px brd1px brdcGray brdrs10px">
  <img class="arV w100% brdrs5px" src="image.jpg" alt="Card image">
  <h3 class="mT15px mB10px cDarkBlue">Card Title</h3>
  <p class="cGray mB15px">Card description text goes here with some details.</p>
  <button class="mT10px p10px;20px bgcBlue cWhite brdrs5px brd0">Read More</button>
</div>
```

This creates a card with:
- Flex column layout (`dF fxdColumn`)
- Padding all around (`p20px`)
- Border with rounded corners (`brd1px brdcGray brdrs10px`)
- Image with 16:9 aspect ratio (`arV`)
- Spacing between elements (`mT15px mB10px`)
- Styled button at the bottom

### Navigation Bar

```html
<nav class="dF jcSb aiC p15px bgcDarkBlue w100%">
  <div class="cWhite fz20px fw700">Logo</div>
  <div class="dF gap20px">
    <a href="#" class="cWhite tdN cBlue@:hover">Home</a>
    <a href="#" class="cWhite tdN cBlue@:hover">About</a>
    <a href="#" class="cWhite tdN cBlue@:hover">Services</a>
    <a href="#" class="cWhite tdN cBlue@:hover">Contact</a>
  </div>
</nav>
```

This creates a navigation bar with:
- Flex layout with space-between (`dF jcSb aiC`)
- Dark blue background (`bgcDarkBlue`)
- Full width (`w100%`)
- White text for logo and links (`cWhite`)
- No text decoration on links (`tdN`)
- Hover effect on links (`cBlue@:hover`)

## Responsive Design

### Responsive Grid

```html
<div class="dG xs:gtc1fr sm:gtc1fr;1fr md:gtc1fr;1fr;1fr lg:gtc1fr;1fr;1fr;1fr gap15px">
  <div class="p20px bgcLightGray">Item 1</div>
  <div class="p20px bgcLightGray">Item 2</div>
  <div class="p20px bgcLightGray">Item 3</div>
  <div class="p20px bgcLightGray">Item 4</div>
</div>
```

This creates a grid that:
- Shows 1 column on extra small screens (`xs:gtc1fr`)
- Shows 2 columns on small screens (`sm:gtc1fr;1fr`)
- Shows 3 columns on medium screens (`md:gtc1fr;1fr;1fr`)
- Shows 4 columns on large screens (`lg:gtc1fr;1fr;1fr;1fr`)

### Responsive Text Size

```html
<h1 class="xs:fz24px sm:fz28px md:fz32px lg:fz36px">Responsive Heading</h1>
<p class="xs:fz14px sm:fz16px md:fz18px">Responsive paragraph text</p>
```

This creates text that:
- Increases in size as the screen gets larger
- Adapts to different device sizes for better readability

### Responsive Layout Changes

```html
<div class="dF fxdColumn md:fxdRow jcSb aiC gap20px">
  <div class="w100% md:w30% p20px bgcLightGray">Sidebar</div>
  <div class="w100% md:w70% p20px bgcWhite">Main Content</div>
</div>
```

This creates a layout that:
- Stacks vertically on mobile (`fxdColumn`)
- Displays side-by-side on medium screens and up (`md:fxdRow`)
- Takes full width on mobile (`w100%`)
- Splits 30/70 on larger screens (`md:w30%`, `md:w70%`)

## Advanced Features

### Layer System for Specificity

```html
<div class="1cRed 2cBlue 3c!Green">
  This text will be green due to layer 3 and the importance marker
</div>
```

This demonstrates:
- Layer 1 sets red color (`1cRed`)
- Layer 2 overrides with blue (`2cBlue`)
- Layer 3 with importance marker takes highest precedence (`3c!Green`)

### Selector Syntax

```html
<button class="p10px;20px bgcBlue cWhite brdrs5px
               bgcDarkBlue@:hover
               bgcGray@:active
               brdcRed@:focus">
  Interactive Button
</button>
```

This creates a button that:
- Has base styling for padding, color, and border radius
- Changes background on hover (`bgcDarkBlue@:hover`)
- Changes background when active (`bgcGray@:active`)
- Shows a red border when focused (`brdcRed@:focus`)

### Combined Properties

```html
<div class="cWhite&bgcBlue&p20px&brdrs10px">
  White text on blue background with padding and rounded corners
</div>
```

This demonstrates combining multiple properties with the `&` character.

### Using Importance Marker

```html
<div class="cRed">
  <span class="cBlue">Blue text</span>
  <span class="c!Green">Green text (with importance)</span>
</div>
```

This shows how the importance marker (`!`) ensures the green color takes precedence.

## Practical Examples

### Login Form

```html
<form class="dF fxdColumn p30px brd1px brdcGray brdrs10px mX20px w100% md:w400px">
  <h2 class="cDarkBlue mB20px tac">Login</h2>
  
  <label class="cGray mB5px">Email</label>
  <input type="email" class="p10px brd1px brdcLightGray brdrs5px w100% mB15px">
  
  <label class="cGray mB5px">Password</label>
  <input type="password" class="p10px brd1px brdcLightGray brdrs5px w100% mB20px">
  
  <button type="submit" class="p10px;20px bgcBlue cWhite brdrs5px brd0 
                               bgcDarkBlue@:hover w100%">
    Sign In
  </button>
  
  <a href="#" class="cBlue tac mT15px tdN cDarkBlue@:hover">Forgot Password?</a>
</form>
```

This creates a complete login form with:
- Flex column layout (`dF fxdColumn`)
- Responsive width (`w100% md:w400px`)
- Styled inputs and labels
- Interactive button with hover state
- Centered text and proper spacing