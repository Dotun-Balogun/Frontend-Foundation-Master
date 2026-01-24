# CSS Display — Lesson 2.4

## What is `display`?
The display property controls:
- How an element flows in the layout
- Whether it takes full width or not
- Whether width/height work

---

## 1️⃣ display: block
Examples:
- div
- p
- h1–h6

Behavior:
- Starts on a new line
- Takes full width by default
- Width & height work

---

## 2️⃣ display: inline
Examples:
- span
- a
- strong

Behavior:
- Stays in text flow
- Width & height are ignored
- Padding works horizontally only

---

## 3️⃣ display: inline-block
Best of both worlds:
- Sits inline
- Width & height work

Very common for:
- Buttons
- Cards
- Nav items

---

## 4️⃣ display: none
- Element is removed from layout
- No space is reserved
- Not accessible to screen readers

⚠️ Important for accessibility:
Use `visibility: hidden` or `aria-hidden`
when appropriate instead.

---

## Common Beginner Confusions

❌ “Why is my width not working?”
→ Element is inline

❌ “Why are elements stacking?”
→ Element is block

❌ “Why is there a gap?”
→ Margins on block elements

---

## Exercises

1. Change `.inline` to `inline-block`
2. Remove `display: none` and observe spacing
3. Set `.block` to `inline`
4. Try `visibility: hidden` instead of `display: none`

---


## Key Takeaway
> If layout feels confusing, check `display` first.
> Most CSS layout issues start here.
