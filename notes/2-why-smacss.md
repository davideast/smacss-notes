# Why SMACSS

Utility classes

```css
.block { display:block !important; }
.inline { display:inline !important; }
.hide { display:none !important; }
.s-none { margin:0 !important; }
.s { margin:10px !important; }
.ss { margin:20px !important; }
.sr { margin-right: 0px !important; }
.p-none { padding:0 !important; }
.p { padding:10px !important; }
.pp { padding:20px !important; }
.pt { padding-top:10px !important; }
.w-auto { width:auto !important; }
```

A few scary things:
1. Naming conventions. Too brief.
2. An abstraction of inline styles.

```css
.layout_1_2 #blogList .pageitem .statusBar {}
.layout_1_2 #blogList .pageitem .statusBar .status {}
.layout_1_2 #blogList .pageitem .statusBar .status .status1 {}
            #blogList .pageitem .statusBar .status {}
.layout_1_2 $blogList .pageitem .statusBar .status .status1 {}
.layout_1_2 $blogList .pageitem .statusBar .status .status1 a {}
.layout_1_2 $blogList .pageitem .statusBar .status .status1 .sep {}
```

Too specific, the real thing we're trying to style is the `.status`.

```css
.statusBar {}
.statusBar .status {}
.statusBar .status .status1 {}
           .status {}
.statusBar .status .status1 {}
.statusBar .status .status1 a {}
.statusBar .status .status1 .sep {}
```

Repeated styles.

```css
#nav-header ul li {
  float: left;
}
#nav-content ul li {
  float: left;
}
```

No code re-use. Codebase gets larger and harder to manage. It will difficult to say "Change a design of a navigation".

```css 
#comments .comment .meta .authorname {}
#comments .comment .meta .commentnumber a {}
```

This is a lot of extra code for little to no reason. This is the important stuff to style:

```css 
.authorname {}
.commentnumber a {}
```

### Inspiration
- Nicole Sullivan's Object-Oriented CSS 
- Jeremy Keith's Pattern Primer
- Natalie Downe's Practical, maintable CSS presentation
- Jina Bolton's CSS Workflow presentation

Move to modules

```css
// Modules
// ---------------------------
@import "btn";
@import "img";
@import "layout";
@import "nav";
@import "tables";
@import "forms";
@import "section";
```

### Why SMACSS?

1. **Categorization** - We're writing CSS for a reason. What are those reasons?
2. **Naming Convention** - Why are we naming things the way they are? How do we separate things between each other? Foundation of SMACSS. It allow us to recoginize when things belong together and when they don't.
3. **Decoupling CSS from HTML** - The cascade can make life difficult. How can we mitigate those issues? How can avoid a bunch of different styles in our CSS trying to style the same thing?
4 **State-based Design** - A reflection of how I look at building a web page. Take a look at the components that we have and how do they exist in different states? 
