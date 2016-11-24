# Base and Layout

We may have a `<div>`, it exists with other HTML elements on the page.

What is this `<div>` doing? What is it doing that's different than all of the other elements on the page?

What is the CSS that I have to write to style this `<div>` to do what I want to do?

### Categorization

#### Base Styles
- Element selectors
- CSS Resets 
- Normalize

+-----------+
|   LAYOUT  |
+-----------+
+-----------+
|   BASE    |
+-----------+

**Base styles** are regular element selectors. No classes, no ids, just element selectors. 

```css 
html {
  background-color: #FFF;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 14px;
}
body {
  margin: 0;
  padding: 0;
}
h1, h2, h3 {
  margin: 1em 0;
}
```
This might be your CSS resets or normalize. This creates the foundation of everything else to be built on. 

Snook keeps his base styles minimal. He doesn't use normalize or CSS resets. He uses a minimal sheet to remove margin & padding from form, body, default background color, but not a whole lot else.

**When you start writing CSS it should be serving a purpose. If you have to write CSS to override other CSS, that's a sign of inefficency.**

### Layout styles

**What are the major layout containers we have on a page?** Header, content, sidebar.

It's not describing the content. It's describing the grouping. It's not about about what is inside the group, it's about the overall structure.

- Major containing elements
- Grid systems
- How do you group your content?

