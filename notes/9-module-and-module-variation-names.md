# Module and Module Variation Names

### Module

Do not prefix modules with `module-` unlike `layout-`.
 
```css
.tab {}
.listview {}
.btn {}
```

It's okay to be a bit verbose in your naming conventions. However, there is not great tooling for minifying css class names.

### Module Variations 

Each variation is prefixed with the module name. Both the base module name, `.btn` and the module variation name have to be included on the same module variation element.

```css
.btn {}
.btn-large {}
.btn-small {}
.btn-default {}
.btn-search {}
```

```html 
<button class="btn btn-large">Click</button>
```

What if the root module has a hyphen in the name, like `.list-view`? Combine the root module name `.listview`, and use the hyphen for module variations.

```css
.btn.large {} /*???*/
```

Doubling up means your specificity is greater. The problem is that you can have several things that the second class applies to.

```css
.btn.large {}
.field.large {}
.modal.large {}
```

**Prefer explicitly obvious vs. small convenience.** 

Determining relations with smaller and less explicit classes is difficult.

Do CSS preprocessors save the day? No.

```css
.btn {
  padding: 5px 10px;
  font-size: 1em;
  .large {
    padding: 10px 20px;
    font-size: 2em;
  }
}
```

There are different contexts to the `.large` class, and determining what it will do and it's relationship to the parent element is difficult.

```css
.btn {
  padding: 5px 10px;
  font-size: 1em;
}

.btn-large {
  padding: 10px 20px;
  font-size: 2em;
}
```

The relationship is obvious, and nesting is not required. 

**Prefer explicit and simple.**
