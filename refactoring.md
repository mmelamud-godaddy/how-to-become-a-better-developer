# Refactoring[^1]
---

> ### Refactor Safely, Refactor Early, Refactor Often!

- Extract Functions/Methods

You have a code fragment that can be grouped together.

```javascript
const cards = getCards();
cards.forEach(function(card) {
  console.log(card);
});
```

Extract the fragment into a new function/method.

```javascript
var logCards = function(cards) {
  posts.forEach(function(card) {
      console.log(card);
  });
};

var cards = getCards();
logCards(cards);
```

- Work to Reduce Cyclomatic Complexity[^2]
- Move Related Concepts Closer Together
- Look Out for Re-Use
- Work in Very Small Steps
- Separate Concerns

[^1]: [Refactoring: Improving the Design of Existing Code](https://www.martinfowler.com/books/refactoring.html) by Martin Fowler, with Kent Beck
[^2]: Cyclomatic Complexity measures the number of linearly independent paths through a program's source code. This rule allows setting a cyclomatic complexity threshold. [Easing into Cyclomatic Complexity](https://dev.to/igneel64/easing-into-cyclomatic-complexity-38b1)
