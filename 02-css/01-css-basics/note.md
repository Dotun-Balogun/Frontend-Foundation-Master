# CSS Basics — Lesson 2

## What is CSS?
CSS (Cascading Style Sheets) controls how HTML elements look.

HTML = structure  
CSS = presentation  

CSS does NOT:
- Add meaning
- Add logic
- Change document structure

---

## Ways to Add CSS

1. Inline CSS (bad for scaling)
2. Internal CSS (inside <style>)
3. External CSS ✅ (best practice)

This lesson uses **external CSS**.

---

## Why CSS Goes in the <head>

- Browser reads HTML top-down
- CSS must load BEFORE rendering
- Prevents layout jumps (FOUC)

---

## The Cascade (Very Important)

CSS follows this priority order:
1. Browser default styles
2. External CSS
3. Internal CSS
4. Inline CSS (highest priority)

Last rule wins **if specificity is equal**.

---

## Key Takeaways

- CSS selects elements
- CSS applies visual rules
- Order matters
- External CSS is standard
