# Using third party libraries

What is your position on third party libraries? Snook hand codes everything. **Every line of code serves a purpose.** Using 3ps can deliver dead code to the user. **Write CSS that is specific to solving the problem.**"

Overriding and changing CSS from 3ps can be problematic and hacking it from the wrong way.

**Identify the problems you want to solve.**

At Shopify Snook and co wanted to make writing frontend code easier for their developers. A lot of them don't understand how CSS, they're great at MySQL, Redis, etc. But can they tie in input to a component without a frontend developer? His goal is design a component to solve that problem.

**Key example:** Grid System.
They had a 24 column grid. span-24, span-23, span-22, etc. How many of these classes were actually used? A quarter went unused. Another quarter used once, maybe twice. They realized they needed to split things into equal columns. Flexbox solved everything. 

**Keep the system simple by evaluating what your needs are.**

Most websites that use a 24 column layout tend to only use a 1-4 column layout.

**Ask: What is the design trying to do? Then come up with the minimal amount of CSS possible to accomplish it.**

**It's okay to use third party libraries. If a third party component solves 95% of your problem, bring 95% of it in and leave the rest.** 