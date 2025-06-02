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
<div class="container">
  <div class="grid">
    <div class="demo-item">
      <h3>opLt</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opLt"
        />
      </div>
    </div>
    <div class="demo-item">
      <h3>opT</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opT"
        />
      </div>
    </div>
    <div class="demo-item">
      <h3>opRt</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opRt"
        />
      </div>
    </div>

    <div class="demo-item">
      <h3>opL</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opL"
        />
      </div>
    </div>
    <div class="demo-item">
      <h3>opC</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opC"
        />
      </div>
    </div>
    <div class="demo-item">
      <h3>opR</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opR"
        />
      </div>
    </div>

    <div class="demo-item">
      <h3>opLb</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opLb"
        />
      </div>
    </div>
    <div class="demo-item">
      <h3>opB</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opB"
        />
      </div>
    </div>
    <div class="demo-item">
      <h3>opRb</h3>
      <div class="image-container">
        <img
          src="layouts/img/nha-trang-beaches-1.webp"
          alt="Beach scene"
          class="w100% h100% opRb"
        />
      </div>
    </div>
  </div>
</div>
```

This comprehensive grid shows how each object-position utility affects the same image. Notice how different parts of the beach scene become visible depending on the positioning value used.

![Object position grid example](./img/object-position/grid.png)
