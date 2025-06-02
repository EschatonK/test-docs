- **Property:** object-position
- **Shorthand:** op  
  Utilities for controlling the position of replaced elements (like images) within their container.

```css
opC {
  object-position: center;
}
opT {
  object-position: top;
}
opB {
  object-position: bottom;
}
opL {
  object-position: left;
}
opR {
  object-position: right;
}
opLt {
  object-position: left top;
}
opRt {
  object-position: right top;
}
opLb {
  object-position: left bottom;
}
opRb {
  object-position: right bottom;
}
```

The `object-position` property specifies the alignment of the replaced element's content within its container. This is particularly useful when combined with `object-fit: cover` or `object-fit: contain` to control which part of the image is visible when the image is cropped or scaled.

## Complete Object Position Grid Example

The following 3x3 grid demonstrates all nine object-position utility classes using the same image. Each position shows how the image is cropped and positioned within identical containers:

```html
<h3>opLt</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opLt"
  />
</div>

<h3>opT</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opT"
  />
</div>

<h3>opRt</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opRt"
  />
</div>

<h3>opL</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opL"
  />
</div>

<h3>opC</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opC"
  />
</div>

<h3>opR</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opR"
  />
</div>

<h3>opLb</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opLb"
  />
</div>

<h3>opB</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opB"
  />
</div>

<h3>opRb</h3>
<div>
  <img
    src="layouts/img/nha-trang-beaches-1.webp"
    alt="Beach scene"
    class="w100% h100% opRb"
  />
</div>
```

This comprehensive grid shows how each object-position utility affects the same image. Notice how different parts of the beach scene become visible depending on the positioning value used.

![Object position grid example](./img/object-position/grid.png)
