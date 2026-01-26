# Flexbox Deep Dive 

## flex-wrap
Controls whether items stay on one line.

- nowrap (default)
- wrap

Use wrap for responsive layouts.

---

## gap
Controls spacing BETWEEN flex items.
Better than margins.

Example:
gap: 20px;

---

## The flex Shorthand

flex: grow shrink basis;

Example:
flex: 1 1 150px;

Means:
- Can grow
- Can shrink
- Preferred size is 150px

---

## flex-grow
Controls how much an item grows relative to others.

Example:
flex-grow: 2;

This item grows twice as fast as others.

---

## flex-shrink
Controls whether an item can shrink.

Example:
flex-shrink: 0;

Item will NOT shrink, even if space is tight.

---

## flex-basis
Defines the initial size before growing/shrinking.

Example:
flex-basis: 300px;

---

## Mental Model (Very Important)

1. Browser lays out items using flex-basis
2. Extra space? → distribute using flex-grow
3. Not enough space? → shrink using flex-shrink

---

## Common Mistakes

❌ Setting width instead of flex-basis  
❌ Forgetting wrap on small screens  
❌ Using margins instead of gap  

---

## Exercises

1. Remove `flex-wrap` and observe overflow
2. Change `flex: 1 1 150px` to `0 1 auto`
3. Make one item fixed-width
4. Try different grow values

---

## Key Takeaway
> Flexbox is about distributing space, not fixed sizing.
