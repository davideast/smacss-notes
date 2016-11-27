# Thoughts on workflow

### CSS at Facebook (CSS in JS)

The problems CSS in JSS tries to solve are similar to what SMACSS tries to solve.
 - Minification
 - Conflicts (everything is global)

What about versioning in a file? Bundling makes this moot. It's more about class names, not file names. Class names clash, file names usually don't.

**Shame.css** 
Creating a file that states these *hacks* don't belong here, and will be addressed. The *shame* file should be be temporary, and used as a last resort.