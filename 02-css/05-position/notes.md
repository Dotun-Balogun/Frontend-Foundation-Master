# CSS Position 

## What is Positioning?
The `position` property controls:
- How an element is placed
- Whether it stays in document flow
- What it is positioned relative to

---

## 1️⃣ position: static
- Default for all elements
- Ignores top, left, right, bottom
- Stays in normal document flow

---

## 2️⃣ position: relative
- Still occupies original space
- Can be nudged using top/left/etc
- Creates a positioning context

IMPORTANT:
Relative does NOT remove the element from flow.

---

## 3️⃣ position: absolute
- Removed from document flow
- Positioned relative to:
  - nearest ancestor with position ≠ static
  - otherwise the viewport

This is why we often add:
position: relative; to the parent.

---

## 4️⃣ position: fixed
- Removed from document flow
- Always relative to viewport
- Stays in place while scrolling

Common uses:
- Floating buttons
- Sticky chat icons
- Navigation bars

---

## (Bonus) position: sticky
- Acts like relative
- Becomes fixed after scroll threshold
- Requires top value

---

## Common Mistakes

❌ Using absolute without a positioned parent  
❌ Expecting relative to remove element from flow  
❌ Forgetting fixed ignores container boundaries  

---

## Exercises

1. Remove `position: relative` from `.container`
2. Change `.absolute` to `relative`
3. Add `position: sticky` with `top: 0`
4. Scroll page to observe `fixed`

---

## Mental Model

STATIC → normal flow  
RELATIVE → normal flow + offset  
ABSOLUTE → removed + parent-based  
FIXED → removed + viewport-based  

---

## Key Takeaway
> Absolute positioning only works correctly
> when you control the parent.
