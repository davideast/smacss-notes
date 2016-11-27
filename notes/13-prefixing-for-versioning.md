# Prefixing for versioning or packaging

At Shopify, they have hundreds of pages. Imagine the PR for modifying the input on every single page, cde review, test, and commit, and merge.

How to progress in small chunks? Versioning the components.

```css
.next-btn {}

.next-btn-is-active {}
.next-btn-is-disabled {}
```

Slowly migrate the design with the versioning. 

Pure CSS is a CSS Framework built by a team at Yahoo. It takes a SMACSS approach.

Every class is prefixed with `pure`. It allows you to identify what belongs to the library vs. you. Their buttons are not going to conflict with your own code or even other libraries.