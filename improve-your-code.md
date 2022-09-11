# 5 Ways to Improve Your Code
---
1. **Comments**

   There's a fine line between comments that illuminate and comments that obscure. Are the comments necessary? Do they explain "why" and not "what"? Can you refactor the code so the comments aren't required? And remember, you're writing comments for people, not machines.

2. **Long Method**

   All other things being equal, a shorter method is easier to read, easier to understand, and easier to troubleshoot. Refactor long methods into smaller methods if you can.

3. **Long Parameter List**

   The more parameters a method has, the more complex it is. Limit the number of parameters you need in a given method, or use an object to combine the parameters.

4. **Duplicate Code**

   > Every piece of knowledge or logic must have a single, unambiguous representation within a system.

   Duplicating code always ends with a mess. If you fixed a bug somewhere you need to re-patch it multiple times. Having less and non-redundant code saves time as well as increases maintainability. *Don't Repeat Yourself!*[^1]

5. **Conditional Complexity**

   Watch out for large conditional logic blocks, particularly blocks that tend to grow larger or change significantly over time. Consider alternative object-oriented approaches such as [decorator](https://www.dofactory.com/javascript/design-patterns/decorator), [strategy](https://www.dofactory.com/javascript/design-patterns/strategy), or [state](https://www.dofactory.com/javascript/design-patterns/state) or their functional programming equivalents: [decorator](https://medium.com/qualyteam-engineering/decorator-design-pattern-in-functional-and-object-oriented-programming-e0a2be3c5679), [state](https://betterprogramming.pub/the-state-design-pattern-in-javascript-4eebdf5e471), or [strategy](https://thomas-rubattel.medium.com/strategy-pattern-in-functional-programming-38ddcc2b2d50).
   
 
 [^1]: ["Don't repeat yourself" (DRY)](https://www.plutora.com/blog/understanding-the-dry-dont-repeat-yourself-principle) is a principle of software development aimed at reducing repetition of software patterns, replacing it with abstractions or using data normalization to avoid redundancy.
