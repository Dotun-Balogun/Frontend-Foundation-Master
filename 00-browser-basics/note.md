Here is your notes file, professionally formatted and organized for clarity. I’ve cleaned up the syntax and structure so you can simply copy and paste it into your `.md` file.

---

# Browser Basics: Script Order & DOM

## 📁 Purpose of This Folder

This folder explains the fundamental lifecycle of a webpage, specifically how the browser:

* **Reads HTML** from top to bottom.
* **Builds the DOM** (Document Object Model).
* **Executes JavaScript** and manages timing.
* **Accesses Elements** and why scripts sometimes fail to "see" them.

---

## 📜 Script Order (`script-order.html`)

### 1. What to Observe

1. Open `script-order.html` in your browser.
2. Open **DevTools → Console**.
3. **Notice:** The script runs, but the `<h1>` is logged as `null`.

### 2. Why This Happens

The browser processes HTML sequentially. When it encounters a `<script>` tag in the `<head>` or middle of the body:

1. It **pauses** HTML parsing.
2. It **executes** the JavaScript immediately.
3. Because the `<h1>` appears *after* the script in the code, it hasn't been parsed yet.

```javascript
// This returns null because the element doesn't exist in the DOM yet
console.log(document.querySelector("h1")); 

```

### 3. How to Fix It

* **Option 1: Move Script to Bottom** Place the `<script>` tag just before the closing `</body>` tag. This ensures the entire DOM is loaded before the script runs.
* **Option 2: Use the `defer` Attribute** Add `defer` to your script tag: `<script src="..." defer></script>`.
* **Effect:** The browser downloads the script in the background but waits to execute it until the HTML parsing is completely finished.



---

## 🌳 DOM Tree (`dom-tree.html`)

### 1. What to Observe

1. Open `dom-tree.html`.
2. **Right-click → Inspect** to see the Elements panel.
3. Observe the hierarchical tree structure:
* `<header>`, `<main>`, and `<footer>` as top-level landmarks.
* Headings and paragraphs nested within their respective parents.



### 2. Why This Matters

* **JavaScript:** Interacts with the DOM tree to change styles, content, or behavior.
* **Accessibility (A11y) ♿:** Screen readers and keyboard navigation rely entirely on a logical tree structure.

> [!IMPORTANT]
> If content is created too late, loaded in the wrong order, or structured with an incorrect hierarchy (e.g., an `<h3>` before an `<h1>`), then **screen readers fail**, **focus order breaks**, and **keyboard users struggle**.

---

## 🛠 Exercises

1. **Reorder:** Move the script tag to the bottom of `script-order.html` and check the console.
2. **Attribute Test:** Move the script back to the `<head>`, add the `defer` attribute, and observe the result.
3. **DOM Manipulation:** Once the script loads correctly, use `document.querySelector("h1").innerText = "Hello World";` to change the text.
4. **Audit:** Inspect the DOM tree in `dom-tree.html` and confirm the nesting matches your expectations.

---

Would you like me to create a small code example for the `defer` vs. `async` attributes to add to your notes?