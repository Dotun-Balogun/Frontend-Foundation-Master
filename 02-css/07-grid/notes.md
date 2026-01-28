# CSS Grid 

## Why Grid Exists
Grid solves:
- Rows AND columns at the same time
- Page-level layouts
- Complex alignment

Flexbox = one direction  
Grid = two directions

---

## Grid Roles

1️⃣ Grid container  
2️⃣ Grid items (direct children)

---

## Defining Columns

grid-template-columns: repeat(3, 1fr);

Means:
- 3 columns
- Each column takes equal space

`fr` = fraction of available space

---

## Rows

grid-auto-rows: 100px;

Every row created automatically is 100px tall.

---

## gap
Spacing between rows and columns.
Better than margins.

---

## Mental Model

Think of:
- Excel sheets
- Graph paper
- Table without table semantics

You place items INTO CELLS.

---

## Common Units

- px → fixed
- % → relative
- fr → flexible (preferred)

---

## Common Mistakes

❌ Mixing grid and flex without reason  
❌ Forgetting grid container  
❌ Overusing fixed pixels  

---

## Exercises

1. Change columns to `repeat(2, 1fr)`
2. Use `grid-template-columns: 200px 1fr`
3. Change row height
4. Remove gap and observe collapse

---

## Key Takeaway
> Grid defines structure first, content second.
