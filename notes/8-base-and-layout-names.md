# Base and Layout Names

**How do we clarify our intent? How do we express what we're trying to do?** How do we write things as a way of grouping them together or keeping them separate from others?

### Base

Element selectors.

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

May have some psuedo-class selectors, but it's all about the styles that apply across the board, so you don't want to be heavy handed.

### Layout

Prefixing the name `layout` signifies that it's a layout element.

```css
.layout-header {
  width: 100%;
}
.layout-sidebar {
  float: left;
  width: 20%;
}
.layout-content {
  float: right;
  width: 80%;
}
```

These are the containers that we're going to put stuff into.

### User Class over ID 
**Specificity is dangerous.**

|  Inline  |    ID    |  Class   |  Element  |
----------------------------------------------
| style="" | #article | .article | a:nth-child


```css
a { color: #039; }
.subdued { color: #666; }
#cancel { color: #900; }
```

```html
<a href="...">Link</a>
<a href="..." class="subdued">Link</a>
<a href="..." id="cancel">Link</a>
<a href="..." id="cancel" class="subdued">Link</a> 
```

Specificity says that the `id` of `cancel` will out rank the `class` of `subdued`.

### Specificty Buster! `!important`
Don't use it.

 ```css
a { color: #039; }
.subdued, #cancel.subdued { color: #666; }
#cancel { color: #900; }
```

This change wins, but we've created two styles and applied them to the same element. Instead you can simplify by have a `subdued` `class` or a `cancel` `class`. 

### Naming Convention

 ```css
a { color: #039; }
.link-subdued { color: #666; }
.link-danger { color: #900; }
```

### Grid Systems

```css
.container_12,
.container_16 {
  margin-left: auto;
  margin-right: auto;
  width: 960px;
}
```

It's okay to use third party library names instead of your convention.

