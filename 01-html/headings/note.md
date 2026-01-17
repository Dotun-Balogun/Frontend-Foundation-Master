# HTML Headings & Document Outline

## Purpose of This Folder
This folder explains:
- How headings define document structure
- Why heading order matters
- How screen readers interpret pages

---

## What Headings Really Are
Headings (`<h1>` – `<h6>`) are **not for size**.
They define **content hierarchy**.

Think of them like:
- A book outline
- A table of contents

---

## Heading Levels Explained
- `<h1>` → Page title (highest level)
- `<h2>` → Major section
- `<h3>` → Subsection
- `<h4>` → Sub-subsection

📌 Headings must be **nested logically**, not visually.

---

## Document Outline (`outline.html`)

### Visual Structure
h1 Frontend Foundation
├─ h2 HTML Basics
│ ├─ h3 Elements
│ └─ h3 Attributes
└─ h2 CSS Basics



This matches how the content is organized.

---

## Accessibility Perspective ♿
Screen readers:
- Use headings to navigate
- Allow users to jump between sections
- Rely on correct order

If you skip levels:
- Navigation becomes confusing
- Context is lost

---

## Common Beginner Mistakes
❌ Using `<h1>` multiple times for styling  
❌ Skipping from `<h1>` to `<h4>`  
❌ Choosing headings based on font size  
❌ Using headings for decoration

---

## Rules to Follow
- One main `<h1>` per page (generally)
- Do not skip heading levels
- Every section should have a heading
- Use CSS to style, not headings

---

## Exercises
1. Change an `<h3>` to `<h4>` and inspect the outline
2. Skip a heading level and note the structure problem
3. Try navigating with keyboard + screen reader tools

---

## Key Takeaway
> Headings describe structure, not appearance.
