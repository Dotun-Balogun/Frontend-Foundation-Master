# CSS Typography - Complete Notes

## Table of Contents
1. [Overview](#overview)
2. [Font Families](#font-families)
3. [Font Properties](#font-properties)
4. [Text Properties](#text-properties)
5. [Spacing & Readability](#spacing--readability)
6. [Advanced Typography](#advanced-typography)
7. [Web Fonts](#web-fonts)
8. [Responsive Typography](#responsive-typography)
9. [Accessibility](#accessibility)
10. [Common Errors to Avoid](#common-errors-to-avoid)
11. [Best Practices](#best-practices)
12. [Quick Reference](#quick-reference)

---

## Overview

Typography is the art and technique of arranging type to make written language legible, readable, and appealing. In web development, good typography:
- Enhances readability and user experience
- Establishes visual hierarchy
- Reinforces brand identity
- Improves accessibility
- Increases engagement and time on page

**Key Principle:** Typography is not just about making things look pretty—it's about making content easy to read and understand.

---

## Font Families

### What are Font Families?
Font families are groups of fonts that share similar design characteristics. CSS allows you to specify multiple fonts as fallbacks.

### Types of Font Families

#### 1. **Serif Fonts**
```css
font-family: Georgia, 'Times New Roman', serif;
```
- Have decorative strokes (serifs) at the ends of letters
- Often perceived as traditional, formal, or elegant
- **Best for:** Print documents, formal content, long-form reading
- **Examples:** Georgia, Times New Roman, Playfair Display

#### 2. **Sans-Serif Fonts**
```css
font-family: Arial, Helvetica, sans-serif;
```
- Clean, without decorative strokes
- Modern, minimalist appearance
- **Best for:** Web interfaces, mobile apps, clean designs
- **Examples:** Arial, Helvetica, Inter, Roboto

#### 3. **Monospace Fonts**
```css
font-family: 'Courier New', monospace;
```
- Each character occupies the same width
- **Best for:** Code blocks, technical documentation, tables
- **Examples:** Courier New, Fira Code, Source Code Pro

### Font Stack Strategy
Always provide fallback fonts in order of preference:

```css
font-family: 'Inter', Arial, Helvetica, sans-serif;
```

**Order:**
1. Your preferred custom font
2. Common alternative fonts
3. Generic family (serif, sans-serif, monospace)

### ⚠️ Common Errors
- ❌ Not providing fallbacks: `font-family: 'MyCustomFont';`
- ❌ Misspelling font names
- ❌ Forgetting quotes for multi-word fonts: `font-family: Times New Roman;` (wrong)
- ✅ Always quote multi-word fonts: `font-family: 'Times New Roman';`

---

## Font Properties

### font-weight
Controls how bold text appears.

```css
font-weight: 300;  /* Light */
font-weight: 400;  /* Normal/Regular */
font-weight: 600;  /* Semi-bold */
font-weight: 700;  /* Bold */
font-weight: 900;  /* Extra-bold */
```

**Keywords:** `normal` (400), `bold` (700), `lighter`, `bolder`

**Key Insight:** Not all fonts support all weights. Use only weights that your chosen font family actually provides.

### font-style
```css
font-style: normal;   /* Default */
font-style: italic;   /* Slanted, designed version */
font-style: oblique;  /* Artificially slanted */
```

**Key Difference:** `italic` uses a designed slanted version, `oblique` just tilts the normal font.

### font-size
```css
/* Absolute units */
font-size: 16px;      /* Pixels */
font-size: 1.2em;     /* Relative to parent */
font-size: 1.2rem;    /* Relative to root */

/* Responsive */
font-size: clamp(1rem, 2vw, 2rem);  /* Min, preferred, max */
```

**Best Practice:** Use `rem` for most font sizes (allows user scaling), `em` for components that should scale with their container.

### font (shorthand)
```css
/* font: [style] [weight] size/line-height family; */
font: italic 600 1.2rem/1.6 Arial, sans-serif;
```

**⚠️ Important:** `font-size` and `font-family` are required when using shorthand.

---

## Text Properties

### text-align
```css
text-align: left;      /* Default for LTR languages */
text-align: center;    /* Centered */
text-align: right;     /* Right-aligned */
text-align: justify;   /* Spreads text evenly */
```

**⚠️ Caution with justify:** Can create awkward spacing. Use sparingly.

### text-decoration
```css
text-decoration: none;              /* Remove decoration */
text-decoration: underline;         /* Underline */
text-decoration: line-through;      /* Strikethrough */
text-decoration: underline dotted;  /* Style variation */
```

**Common Use:** Removing underlines from links:
```css
a {
    text-decoration: none;
}
```

### text-transform
```css
text-transform: uppercase;    /* ALL CAPS */
text-transform: lowercase;    /* all lowercase */
text-transform: capitalize;   /* Capitalize Each Word */
text-transform: none;         /* Original */
```

**Accessibility Note:** Screen readers may not properly announce transformed text. Use semantic HTML when meaning matters.

---

## Spacing & Readability

### line-height (Leading)
Controls vertical spacing between lines.

```css
line-height: 1.5;    /* Unitless - recommended */
line-height: 24px;   /* Fixed */
line-height: 150%;   /* Percentage */
```

**Best Practices:**
- Body text: `1.5` to `1.8`
- Headings: `1.2` to `1.3`
- Short lines: can be tighter
- Long lines: need more space

**⚠️ Use Unitless Values:** `line-height: 1.5` (not `1.5em`) prevents inheritance issues.

### letter-spacing (Tracking)
```css
letter-spacing: normal;    /* Default */
letter-spacing: 0.05em;    /* Slight increase */
letter-spacing: -0.02em;   /* Tighter */
```

**Use Cases:**
- Uppercase text often needs more letter spacing
- Small text may benefit from slightly increased spacing
- Large headings can use tighter spacing

### word-spacing
```css
word-spacing: normal;
word-spacing: 0.2em;
```

**Rarely Used:** Most designs work fine with default word spacing.

---

## Advanced Typography

### text-shadow
```css
text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
/*           x   y   blur color */
```

**Multiple Shadows:**
```css
text-shadow: 
    1px 1px 0 #fff,
    2px 2px 0 rgba(0, 0, 0, 0.3);
```

**⚠️ Performance:** Heavy shadows can impact rendering. Use sparingly.

### text-overflow
```css
.truncate {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    max-width: 300px;
}
```

**Result:** "This is a very long text th..."

**All Three Properties Required:** Won't work with just one or two.

### white-space
```css
white-space: normal;    /* Default: collapses spaces */
white-space: nowrap;    /* Prevents wrapping */
white-space: pre;       /* Preserves all spaces and breaks */
white-space: pre-wrap;  /* Preserves spaces but allows wrapping */
```

**Use Case:** Preventing text from wrapping in buttons or labels.

### Hyphenation & Word Breaking
```css
/* Enable automatic hyphenation */
hyphens: auto;

/* Break long words */
word-break: break-word;
overflow-wrap: break-word;
```

**Language Requirement:** `hyphens` requires proper `lang` attribute in HTML:
```html
<html lang="en">
```

---

## Web Fonts

### Using Google Fonts

**Step 1: Link in HTML**
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet">
```

**Step 2: Use in CSS**
```css
body {
    font-family: 'Inter', sans-serif;
}
```

### @font-face (Self-Hosting)
```css
@font-face {
    font-family: 'MyCustomFont';
    src: url('/fonts/mycustomfont.woff2') format('woff2'),
         url('/fonts/mycustomfont.woff') format('woff');
    font-weight: 400;
    font-style: normal;
    font-display: swap; /* Prevents invisible text during loading */
}
```

**Font Formats:**
- **WOFF2:** Best compression, modern browsers (use first)
- **WOFF:** Fallback for older browsers
- **TTF/OTF:** Larger files, use as last resort

### font-display Property
```css
font-display: swap;    /* Show fallback immediately, swap when loaded */
font-display: block;   /* Invisible text while loading */
font-display: fallback;/* Brief invisible period, then fallback */
font-display: optional;/* Use only if loads fast, else fallback */
```

**Recommendation:** Use `swap` for better user experience.

### ⚠️ Performance Considerations
- Limit number of font families (2-3 max)
- Load only weights you actually use
- Use `preconnect` for external font providers
- Consider system font stacks for better performance

### System Font Stack (No Download Needed)
```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto',
    'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans',
    'Helvetica Neue', sans-serif;
```

**Advantage:** Zero loading time, native look on each OS.

---

## Responsive Typography

### Using clamp()
Modern, responsive font sizing:

```css
font-size: clamp(1rem, 2vw + 0.5rem, 2rem);
/*         min   preferred    max */
```

**How it works:** Font grows with viewport but never smaller than 1rem or larger than 2rem.

### rem vs em

**rem (Root EM):**
- Relative to root `<html>` font size
- Consistent scaling
- **Best for:** Global sizing, components that shouldn't compound

```css
html { font-size: 16px; }
p { font-size: 1.125rem; } /* Always 18px */
```

**em:**
- Relative to parent element
- Compounds with nesting
- **Best for:** Component-relative sizing (padding, margins)

```css
.container { font-size: 1.2em; }
.container p { font-size: 1.2em; } /* 1.2 × 1.2 = 1.44× parent! */
```

### Viewport Units
```css
font-size: 5vw;   /* 5% of viewport width */
font-size: 3vh;   /* 3% of viewport height */
```

**⚠️ Warning:** Pure viewport units can become too large or small. Use `clamp()` for safety.

### Media Queries
```css
/* Mobile first */
body {
    font-size: 16px;
}

@media (min-width: 768px) {
    body {
        font-size: 18px;
    }
}

@media (min-width: 1024px) {
    body {
        font-size: 20px;
    }
}
```

---

## Accessibility

### Color Contrast
**WCAG Requirements:**
- **Normal text:** 4.5:1 minimum contrast ratio
- **Large text (18pt+/14pt bold+):** 3:1 minimum
- **AAA Level:** 7:1 for normal, 4.5:1 for large

**Tools:**
- WebAIM Contrast Checker
- Chrome DevTools (Accessibility panel)

### Line Length
**Optimal:** 50-75 characters per line (about 8-12 words)

```css
p {
    max-width: 65ch; /* 65 characters */
}
```

**Why it matters:** Too long = eye strain, too short = choppy reading.

### Font Size Minimums
- Never use font sizes smaller than 14px for body text
- Minimum 16px recommended for comfortable reading
- Use relative units (`rem`) so users can adjust in browser settings

### Scalability
```css
/* ❌ Bad: Fixed pixel sizes prevent user scaling */
html {
    font-size: 16px;
}

/* ✅ Good: Allows user browser settings to apply */
html {
    font-size: 100%; /* Respects user preference */
}
```

### Focus States for Text Links
```css
a:focus {
    outline: 2px solid #4A90E2;
    outline-offset: 2px;
}
```

**Never:** Remove focus outlines without providing an alternative!

### Text Alternatives
```css
/* Using all caps for emphasis - screen readers may spell out */
.uppercase { text-transform: uppercase; }
```

**Better:** Use semantic HTML:
```html
<strong>Important text</strong> <!-- Announced as emphasized -->
```

---

## Common Errors to Avoid

### 1. **Not Setting Base Font Size**
```css
/* ❌ Bad */
p { font-size: 16px; }
h1 { font-size: 32px; }
h2 { font-size: 24px; }

/* ✅ Good */
html { font-size: 100%; }
p { font-size: 1rem; }
h1 { font-size: 2rem; }
h2 { font-size: 1.5rem; }
```

### 2. **Overusing !important**
```css
/* ❌ Bad */
p { font-size: 16px !important; }

/* ✅ Good: Use specificity correctly */
.article p { font-size: 16px; }
```

### 3. **Too Many Font Families**
```css
/* ❌ Bad: Performance killer */
h1 { font-family: 'Font1', sans-serif; }
h2 { font-family: 'Font2', sans-serif; }
p { font-family: 'Font3', sans-serif; }

/* ✅ Good: 2-3 fonts max */
h1, h2 { font-family: 'Playfair Display', serif; }
body { font-family: 'Inter', sans-serif; }
code { font-family: 'Fira Code', monospace; }
```

### 4. **Forgetting Line Height**
```css
/* ❌ Bad: Hard to read */
p {
    font-size: 16px;
}

/* ✅ Good */
p {
    font-size: 16px;
    line-height: 1.6;
}
```

### 5. **Poor Contrast**
```css
/* ❌ Bad: Light gray on white */
p {
    color: #d3d3d3;
    background: #ffffff;
}

/* ✅ Good: Dark text on light background */
p {
    color: #333333;
    background: #ffffff;
}
```

### 6. **Using px for Everything**
```css
/* ❌ Bad: Not scalable */
body { font-size: 16px; }
h1 { font-size: 32px; }

/* ✅ Good: Scalable */
body { font-size: 1rem; }
h1 { font-size: 2rem; }
```

### 7. **Text Overflow Without Handling**
```css
/* ❌ Bad: Text runs off screen */
.truncate {
    max-width: 200px;
}

/* ✅ Good: Properly handled */
.truncate {
    max-width: 200px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}
```

### 8. **Uppercase Everything**
```css
/* ❌ Bad: Hard to read, accessibility issues */
h1 {
    text-transform: uppercase;
    letter-spacing: 0;
}

/* ✅ Good: Use sparingly, add letter spacing */
.label {
    text-transform: uppercase;
    letter-spacing: 0.05em;
    font-size: 0.875rem;
}
```

---

## Best Practices

### 1. **Establish Typography Scale**
```css
:root {
    --font-size-xs: 0.75rem;   /* 12px */
    --font-size-sm: 0.875rem;  /* 14px */
    --font-size-base: 1rem;    /* 16px */
    --font-size-lg: 1.125rem;  /* 18px */
    --font-size-xl: 1.25rem;   /* 20px */
    --font-size-2xl: 1.5rem;   /* 24px */
    --font-size-3xl: 1.875rem; /* 30px */
    --font-size-4xl: 2.25rem;  /* 36px */
}
```

### 2. **Use CSS Variables for Consistency**
```css
:root {
    --font-primary: 'Inter', sans-serif;
    --font-heading: 'Playfair Display', serif;
    --font-mono: 'Fira Code', monospace;
}

body { font-family: var(--font-primary); }
h1, h2, h3 { font-family: var(--font-heading); }
code, pre { font-family: var(--font-mono); }
```

### 3. **Mobile-First Typography**
```css
/* Start with mobile sizes */
body { font-size: 1rem; }
h1 { font-size: 2rem; }

/* Scale up for larger screens */
@media (min-width: 768px) {
    body { font-size: 1.125rem; }
    h1 { font-size: 2.5rem; }
}
```

### 4. **Readable Body Text**
```css
body {
    font-family: -apple-system, sans-serif;
    font-size: 1rem;
    line-height: 1.6;
    color: #333;
    max-width: 70ch;
    margin: 0 auto;
}
```

### 5. **Clear Visual Hierarchy**
```css
h1 { font-size: 2.5rem; font-weight: 700; }
h2 { font-size: 2rem; font-weight: 600; }
h3 { font-size: 1.5rem; font-weight: 600; }
p { font-size: 1rem; font-weight: 400; }
```

### 6. **Performance Optimization**
- Use `font-display: swap` for web fonts
- Limit font variations (weights/styles)
- Subset fonts (include only needed characters)
- Use WOFF2 format first

### 7. **Test Readability**
- Test on actual devices
- Check in different lighting
- Verify color contrast
- Test with browser text size adjustments

---

## Quick Reference

### Font Properties
```css
font-family: 'Font Name', fallback, generic;
font-size: 1rem | 16px | 1em | 2vw;
font-weight: 100-900 | normal | bold;
font-style: normal | italic | oblique;
line-height: 1.5 | 24px | 150%;
```

### Text Properties
```css
text-align: left | center | right | justify;
text-decoration: none | underline | line-through;
text-transform: uppercase | lowercase | capitalize;
letter-spacing: normal | 0.05em | 2px;
word-spacing: normal | 0.2em;
```

### Advanced
```css
text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
text-overflow: clip | ellipsis;
white-space: normal | nowrap | pre;
hyphens: none | auto;
word-break: normal | break-all | break-word;
```

### Responsive
```css
font-size: clamp(1rem, 2vw, 2rem);
@media (min-width: 768px) { /* styles */ }
```

---

## Resources & Further Reading

### Tools
- **Google Fonts:** https://fonts.google.com
- **Font Squirrel:** https://www.fontsquirrel.com
- **Contrast Checker:** https://webaim.org/resources/contrastchecker/
- **Type Scale Generator:** https://type-scale.com

### Typography Principles
- Maintain consistent vertical rhythm
- Use modular scale for font sizes
- Limit font families to 2-3
- Prioritize readability over aesthetics
- Test on real devices

### Accessibility
- WCAG 2.1 Guidelines
- Minimum 4.5:1 contrast for normal text
- Allow text resizing up to 200%
- Never rely on color alone for meaning

---

## Practice Exercises

1. **Create a typography system** using CSS variables for 3 font families
2. **Build a blog post layout** with proper hierarchy and spacing
3. **Make a responsive heading** that scales smoothly across all viewport sizes
4. **Test contrast ratios** for your color combinations
5. **Implement truncation** with ellipsis for long titles
6. **Create accessible link styles** with proper focus states
7. **Build a card component** with balanced typography
8. **Design a pull quote** with italic text and border styling

---

## Key Takeaways

✅ **Typography makes or breaks user experience**  
✅ **Always provide font fallbacks**  
✅ **Use relative units (rem) for scalability**  
✅ **Line height of 1.5-1.8 for body text**  
✅ **Maintain 4.5:1 minimum contrast ratio**  
✅ **Limit line length to 50-75 characters**  
✅ **Test on real devices and different sizes**  
✅ **Performance matters: limit web fonts**  
✅ **Accessibility is not optional**  
✅ **Consistency creates professional designs**

---

**Next Lesson:** CSS Colors & Backgrounds
