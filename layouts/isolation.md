- **Property:** isolation
- **Shorthand:** is  
  Utilities for controlling the isolation of an element from its parent stacking context.

```css
isI {
  isolation: isolate;
}
isA {
  isolation: auto;
}
```

The `isolation` property controls whether an element creates a new stacking context. This is particularly useful for containing CSS blend modes, filters, and other effects that should not interact with elements outside their container.

## Isolation Auto

```css
isA {
  isolation: auto;
}
```

The default value that allows elements to participate in their parent's stacking context. Elements with `isolation: auto` do not create a new stacking context unless other properties force one.

**Example:**

<div class="is">
  <!-- ... -->
</div>

## Isolation Isolate

```css
isI {
  isolation: isolate;
}
```

Creates a new stacking context, isolating the element and its children from the parent stacking context. This is essential for containing blend modes and preventing unwanted interactions.
