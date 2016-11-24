# Solution 1

```css
body { background-color: #333; }
/* Naming convention - these are layout elements */
/* The 1 and 2 is call out to h1, h2, h3 etc.. */
.layout-highlight1 { background-color: #CCC; }
.layout-highlight2 { background-color: #CCC; }
/* 
Come up with a name that is descriptive of what
it's actually doing rather than list classes.
main, .footer, .header { width: 760px; }*/
.layout-constrained { width: 760px; }
.layout-content {}
.layout-sidebar {}

```

```html
<div>
  <div class="layout-constrained"></div>
</div>
<div class="layout-highlight">
  <div class="layout-constrained"></div>
</div>
<div>
  <div class="layout-constrained"></div>
</div> 
```

The site uses a *fixed-width* design. This means that the `header` and `footer` share this contrained design. This requires us to have one parent `div` to go edge to edge, and one child `div` to be constrained.

The header and the footer share the same background color. We need to write a style that shows that they are different or that the main content is different.

**Identify repeating patterns, create class names that help identify what they are.**
