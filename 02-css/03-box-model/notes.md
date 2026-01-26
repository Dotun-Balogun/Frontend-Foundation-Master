# CSS Box Model

## What is the Box Model?
Every HTML element is treated as a rectangular box.

The box has **4 layers**:

1. Content
2. Padding
3. Border
4. Margin

---

## 1️⃣ Content
- The actual text, image, or element content
- Width and height apply ONLY to content by default

---

## 2️⃣ Padding
- Space INSIDE the box
- Pushes content away from the border
- Increases the visual size of the element

Example:
padding: 20px;

---

## 3️⃣ Border
- Wraps around padding and content
- Adds to the total size of the element

Example:
border: 5px solid black;

---

## 4️⃣ Margin
- Space OUTSIDE the element
- Creates distance between elements
- Does NOT affect background or border

Example:
margin: 20px;

---

## Total Width Calculation (Important)

If:
width = 200px  
padding = 20px  
border = 5px  

Total width becomes:

200 (content)
+ 40 (left + right padding)
+ 10 (left + right border)
= 250px

This surprises beginners a lot.

---

## box-sizing (VERY IMPORTANT)

Default:
box-sizing: content-box;

Better option:
box-sizing: border-box;

With border-box:
- width includes padding + border
- layout becomes predictable

---

## Recommended Global Rule

Apply this to ALL projects:

* {
  box-sizing: border-box;
}

---

## Exercises

1. Increase padding and observe size change  
2. Remove margin and compare spacing  
3. Add `box-sizing: border-box` and observe behavior  
4. Try different border widths  

---

## Key Takeaway
> Most CSS layout bugs come from misunderstanding the box model.
> Master this and layouts stop feeling “random”.
