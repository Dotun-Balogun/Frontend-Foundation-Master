# Flexbox 

## Why Flexbox Exists
Flexbox solves:
- Horizontal alignment
- Vertical centering
- Equal spacing
- Responsive layouts

Without hacks.

---

## Two Important Roles

1️⃣ Flex container  
2️⃣ Flex items (direct children only)

Only DIRECT children are flex items.

---

## Main Axis vs Cross Axis

Default:
- Main axis → horizontal
- Cross axis → vertical

If `flex-direction: column`:
- Main axis → vertical
- Cross axis → horizontal

---

## Key Properties (Container)

### display: flex
Activates flexbox.

### flex-direction
Controls direction:
- row (default)
- column

### justify-content (MAIN axis)
- flex-start
- center
- space-between
- space-around
- space-evenly

### align-items (CROSS axis)
- stretch (default)
- center
- flex-start
- flex-end

---

## Common Beginner Confusion

❌ “Why is align-items not working?”
→ Container has no height

❌ “Why isn’t justify-content vertical?”
→ You’re thinking wrong axis

---

## Exercises

1. Change `justify-content` to `center`
2. Change `flex-direction` to `column`
3. Add `gap: 20px`
4. Remove height and observe alignment changes

---

## Key Takeaway
> Flexbox aligns ITEMS, not content.
> Always think in axes.
