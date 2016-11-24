# Module

+-----------+
|   MODULE  |
+-----------+
+-----------+
|   LAYOUT  |
+-----------+
+-----------+
|   BASE    |
+-----------+

Now that we have layout containers, we need to put something in them. These are the **modules**.

Modules are the content pieces.

Tabs, Buttons, List View. These are the things that are going to contain our content.

- Contain content
- Are the majority of your site
- Each module is an interface that your users have to learn
- Each module is code that has to be written, delivered, and maintained.

Each module you create is an interface that your users need to learn. 

**As you look at your modules ask, how much is that growing? If it's growing to far, there's an opportunity to recognize and pair back the growth.**

### Module Variations (sub-modules)

A module may have variations. It might need to appear in a slightly different way. 

Like buttons, dark, small, search, large. Each button shares similar properties, they have the same font-size and border-radius, but only a few things needed to be different.

**When you're building modules out, we tend to look at things based on the context of where they are.** A button can have a dropdown when clicked. An autocomplete can have a dropdown when input is entered. We tend to look at the autocomplete as one big component and the button as another. However, they have a dropdown and this should be shared code. A benefit of this technique is that you reuse existing patterns. 

### Module child elements (sub-components)

A module is one particular element. There are often module modules that have child elements that relate to that root module. We want to associate these module child elements with that root node.

For example a modal dialog, the content can be different any number of times. There's a recurring pattern for the header and buttons, but the content can be different. You need a way of identifying that HTML for the header and one for the footer and associate them with the root module.

Module isolation is important. This is it's own thing that is separate from other HTML elements on the page. You also want to isolate it from other child elements. 

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

- Isolate Modules from each other
- Prevent styles from coming in or out
