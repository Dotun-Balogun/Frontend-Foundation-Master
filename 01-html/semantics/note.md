# HTML Semantics — Landmarks & Meaning

## Purpose of This Folder
This folder focuses on **semantic HTML**:
- Using tags that describe meaning, not appearance
- Structuring pages so browsers, screen readers, and search engines understand them

---

## What Are Semantic Elements?
Semantic elements describe **what content is**, not how it looks.

Examples:
- `<header>` → introductory content
- `<nav>` → navigation links
- `<main>` → main page content
- `<section>` → thematic grouping
- `<article>` → standalone content
- `<aside>` → related but separate content
- `<footer>` → closing content

---

## Why Semantics Matter
1. Accessibility (screen readers)
2. SEO (search engines)
3. Maintainability (future developers)
4. JavaScript relies on structure

📌 A `<div>` has no meaning.  
A `<section>` does.

---

## Landmarks (`landmarks.html`)

### What to Observe
1. Open the file in a browser
2. Open DevTools → Elements
3. Notice the clear page structure
4. Use DevTools → Accessibility tree (if available)

---

## Screen Reader Perspective
Screen readers use landmarks to:
- Jump to navigation
- Skip repetitive content
- Understand hierarchy

Without landmarks:
- Pages become long, confusing lists

---

## Common Beginner Mistakes
❌ Using `<div>` for everything  
❌ Multiple `<main>` elements  
❌ Skipping heading levels (h1 → h3)  
❌ Using `<section>` without a heading

---

## Accessibility Rules ♿
- Only **one** `<main>` per page
- Headings must be hierarchical
- Use `<nav>` only for major navigation
- Every `<section>` should have a heading

---

## Exercises
1. Replace all semantic tags with `<div>` — observe the DOM
2. Change them back — observe accessibility tree
3. Add another `<article>` and ensure heading order remains correct

---

## Key Takeaway
> HTML is about meaning first. Styling comes later.
