# How CSS Works Behind the Scenes

## Three Pillars to Good HTML / CSS

1. Responsive Design
    - Fluid layouts
    - Media queries
    - Responsive images
    - Correct units
    - Mobile-first design
2. Maintainable & Scalable Code
    - Clean
    - Easy-to-understand
    - Growth
    - Reusable
    - How to organize files
    - How to name classes
    - How to structure HTML
3. Web Performance
    - Less HTTP requests
    - Less code
    - Compress code
    - Use a CSS preprocessor
    - Less images
    - Compress images

## Block Element Modifier

--Block: standalone component that is meaningful on its own.

--Element: part of a block that has no standalone meaning.

--Modifier: a different version of a block or an element.

```css
/* Block component */
.block {
}

/* Element that depends upon the block */
.block__element {
}

/* Modifier that changes the style of the block */
.block--big {
}

.block__element--modifier {
}
```
