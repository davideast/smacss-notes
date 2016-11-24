# State Names

### Naming Conventions

Naming conventions clarify intent.

### Prefix

- Prefix sub-modules with the name of module.
- Helps identify that these things are related


### Module child elements (sub-components)
 
```html
<div class="modal modal-large">
  <form>
    <div class="modal-header">
      <h2>Heading</h2>
      <button class="btn btn-clean">Close</button>
    </div>
    <div class="modal-footer">
      <button class="btn">Cancel</button>
      <button class="btn btn-go">Save</button>
    </div> 
  </form>
</div>
```

`modal` and `modal-large` are together, because `modal` is the module and `modal-header` is the module variation.

Notice that `modal-header` is by itself. It's a module child element. 

`modal` - Module
`modal-large` - Module variation
`modal-header`- Module child elements 

### State

States are like module variations, but they're indicating that JavaScript will be changing things. This is done by adding another prefix `is-`.

```css
.btn {}
.is-btn-active {}
.is-btn-disabled {}
```

Is the button active? Is the button disabled? Sounds like a weird *"I'm Ron Burgundy?"* question. 

New version using `-is-`:

```css
.btn {}
.btn-is-active {}
.btn-is-disabled {}
```

By clarifing the `-is` you state that JavaScript is coming in here and add or remove this class. It's a toggleable state, it's on or off.

You may have some JavaScript that changes states using class names without CSS dependencies. Using a `js-` prefix. They have no css in the elements, but it allows JavaScript to bind to them.

### Prefix

- Prefix states with `is-`:
- `is-` prefix indicates likelihood of JavaScript dependency
- `is-` indicates a toggleable state 
- States that are specific to a module should include the module name.

