# HTML Tables & Lists — Meaningful Data

## Purpose
Lists and tables are for **structured data**, not layout.

---

## Lists Explained
- `<ul>` → unordered list (no priority)
- `<ol>` → ordered list (sequence matters)
- `<li>` → list item

Use lists when:
- Order matters (steps)
- Grouping similar items

---

## Tables Explained
Tables are for:
- Data relationships
- Comparisons
- Rows and columns

NOT for page layout.

---

## Table Structure
- `<table>` → container
- `<thead>` → column headers
- `<tbody>` → data rows
- `<th>` → header cell
- `<td>` → data cell

Screen readers rely on `<th>` to provide context.

---

## Accessibility Notes ♿
- Always use `<th>` for headers
- Keep tables simple
- Avoid merging cells unless necessary
- Tables should be readable line by line

---

## Common Mistakes
❌ Using tables for layout  
❌ Missing `<thead>`  
❌ Styling lists instead of using lists  
❌ Long complex tables without headers

---

## Exercises
1. Convert a paragraph list into `<ul>`
2. Add another column to the table
3. Inspect table structure in DevTools

---

## Key Takeaway
> Use HTML elements for what they mean, not how they look.
