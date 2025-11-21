
### Flexbox Tricky Scenario Discussion:

One common pitfall when using Flexbox is the "equal height cards" challenge. When you have cards with 
varying amounts of content, they naturally want to have different heights. This can lead to an uneven, 
messy-looking grid.

### To solve this, I've used a combination of techniques from the CSS-Tricks Flexbox guide:

1. Made each card a flex container with flex-direction: column
2. Used flex: 1 on the card's paragraph element to make it expand and push the button to the bottom
3. Ensured the cards themselves don't grow beyond their intended width with flex-grow: 0

### This approach ensures that all cards in a row have the same height, with their buttons aligned at the bottom, regardless of content length. Without these flexbox properties, cards with less content would be shorter than their neighbors, creating a jagged, unaligned appearance.

### Another common issue is unexpected wrapping behavior.
By using flex-basis with calc() and setting 
appropriate flex-shrink and flex-grow values, we can control exactly how the cards behave when the 
viewport changes size.
*/