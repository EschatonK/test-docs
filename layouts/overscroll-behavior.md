- **Property:** overscroll-behavior
- **Shorthand:** osrbh
  Utilities for controlling the browser's behavior when reaching the boundary of a scrolling area.

```css
osrbhA {
  overscroll-behavior: auto;
}
osrbhC {
  overscroll-behavior: contain;
}
osrbhN {
  overscroll-behavior: none;
}
```

The `overscroll-behavior` property controls what happens when a user reaches the scrolling boundary of an element. It determines whether to allow scroll chaining to parent elements, enable bounce effects, or disable overscroll behaviors entirely.

## Overscroll Behavior Auto

```css
osrbhA {
  overscroll-behavior: auto;
}
```

Allows the default browser overscroll behavior. When the user reaches the scroll boundary, scrolling continues to the parent element (scroll chaining) and may trigger browser-specific effects like bounce or refresh.

**Example:**

```html
<div class="osrbhA oflAuto">
  <!-- ... -->
</div>
```

## Overscroll Behavior Contain

```css
osrbhC {
  overscroll-behavior: contain;
}
```

Prevents scroll chaining to parent elements but allows local overscroll effects within the element itself. The scrolling action is contained within the element boundary.

**Example:**

```html
<div class="osrbhC oflAuto">
  <!-- ... -->
</div>
```

## Overscroll Behavior None

```css
osrbhN {
  overscroll-behavior: none;
}
```

Completely disables overscroll behavior. No scroll chaining occurs and no local overscroll effects are shown. Scrolling stops completely at the element boundary.

**Example:**

```html
<div class="osrbhN oflAuto">
  <!-- ... -->
</div>
```

## Directional Overscroll Control

### Overscroll Behavior X (Horizontal)

```css
osrbxA {
  overscroll-behavior-x: auto;
}
osrbxC {
  overscroll-behavior-x: contain;
}
osrbxN {
  overscroll-behavior-x: none;
}
```

Controls horizontal overscroll behavior independently from vertical overscroll behavior.

### Overscroll Behavior Y (Vertical)

```css
orsbyA {
  overscroll-behavior-y: auto;
}
orsbyC {
  overscroll-behavior-y: contain;
}
orsbyN {
  overscroll-behavior-y: none;
}
```

Controls vertical overscroll behavior independently from horizontal overscroll behavior.
