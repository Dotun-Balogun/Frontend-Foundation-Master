# CSS Selectors — Targeting HTML Elements

## Purpose
Selectors define **which elements CSS rules apply to**.

---

## Types of Selectors

### 1️⃣ Element Selector
- Targets elements by tag name
- Example: `p { color: red; }`
- All `<p>` tags are affected

### 2️⃣ Class Selector
- Targets elements by class
- Example: `.highlight { background: yellow; }`
- Can target multiple elements

### 3️⃣ ID Selector
- Targets a unique element
- Example: `#intro { font-weight: bold; }`
- Should appear **only once per page**

### 4️⃣ Descendant Selector
- Targets elements inside another element
- Example: `div p { font-style: italic; }`
- Very common in layouts

### 5️⃣ Attribute Selector
- Targets elements based on attributes
- Example: `a[target="_blank"] { color: red; }`
- Useful for links, inputs, images, etc.

### 6️⃣ Pseudo-classes
- Targets elements in a specific state
- Example: `li:first-child` → first list item
- Others: `:hover`, `:nth-child(n)`, `:focus`, `:checked`

### 7️⃣ Pseudo-elements
- Adds content or style to part of an element
- Example: `h1::before { content: "🔥"; }`
- Others: `::after`, `::first-letter`, `::first-line`

---

## Tips
- Class selectors are **preferred** for styling multiple elements
- ID selectors are **unique**, rarely used for styling
- Combine selectors for precision (e.g., `.card p`)

---

## Exercises

1. Change the color of `.highlight` paragraphs to blue  
2. Add a pseudo-class to `<a>` for `:hover` effect  
3. Add `::after` content to `<p>` elements  
4. Experiment with descendant selectors: `ul li:first-child`  

---

## Key Takeaway
> CSS only works when you **target elements correctly**. Choosing the right selector is **the most critical skill in CSS**.
