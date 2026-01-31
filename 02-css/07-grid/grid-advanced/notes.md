# CSS Grid Advanced 

## Grid Areas
Grid areas let you name parts of your layout.

Instead of thinking in numbers:
grid-column: 1 / 3;

You think in words:
header, sidebar, content, footer

This improves readability and maintenance.

---

## grid-template-areas

Each row is a string.
Each word is a column cell.

"header header"
"sidebar content"
"footer footer"

Must match column count.

---

## Responsive Thinking
Grid areas can change per screen size.

Example:
- Desktop: sidebar + content
- Mobile: stacked layout

---

## min-height
Ensures layout stretches even with little content.

---

## auto vs fr
- auto → content-based size
- fr → flexible space

---

## Common Mistakes

❌ Misspelling area names  
❌ Mismatch between columns and areas  
❌ Overcomplicating grid when flex is enough  

---

## Exercises

1. Swap sidebar and content positions
2. Change sidebar width
3. Stack all areas vertically
4. Add media query and change grid areas

---

## Key Takeaway
> Grid areas let you design layouts like a blueprint.
