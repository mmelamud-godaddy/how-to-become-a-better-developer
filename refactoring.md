# Refactoring
---

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

- Work to Reduce Cyclomatic-Complexity
- Move Related Concepts Closer Together
- Look Out for Re-Use
- Work in Very Small Steps
- Separate Concerns
