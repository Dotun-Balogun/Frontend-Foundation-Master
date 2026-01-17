
# HTML Forms — Structure & Accessibility

## Purpose

Forms are the primary way users:

* Send data
* Authenticate
* Interact with applications

They are also one of the **most common accessibility failure points** on the web.

---

## Core Form Elements

* **Form**
  Wraps all user input and defines where data is sent.

* **Label**
  Describes what an input is for.

* **Input**
  Collects user data (text, email, password, etc.).

* **Button**
  Triggers an action such as submitting a form.

---

## Labels Are NOT Optional ♿

Every input **must** have a label.

### Why labels matter

* Screen readers announce the label when the input is focused.
* Clicking a label focuses the corresponding input.
* Improves usability for all users, not only those using assistive technology.

If an input has no label, many users cannot understand what the field is for.

---

## Name vs ID (Very Important)

* **ID**

  * Connects a label to an input.
  * Must be unique on the page.
  * Used by browsers and assistive technologies.

* **Name**

  * Identifies the data when it is sent to the server.
  * Becomes the key in the submitted data.

**Both are required**, but they serve different purposes.

---

## Common Beginner Mistakes ❌

* Using placeholder text instead of a label.
* Forgetting the name attribute on inputs.
* Reusing the same ID for multiple inputs.
* Creating buttons without specifying their purpose.
* Assuming visual clarity equals accessibility.

---

## Accessibility Rules ♿

* One label per input.
* Always use semantic input types (email, password, number, etc.).
* Do not rely on placeholder text for instructions.
* Button text must clearly describe the action.
* Forms must be usable with only a keyboard.

---

## Why Placeholders Are Not Labels

* Placeholders disappear when users start typing.
* Screen readers may not announce placeholders reliably.
* Users with memory or cognitive challenges lose context.

Placeholders are **hints**, not replacements for labels.

---

## Buttons and Actions

* Buttons should clearly state what will happen.
* Avoid vague text like “Click here” or “Submit”.
* Clear actions reduce user errors and confusion.

---

## Exercises (Accessibility Practice)

* Remove a label and try navigating with the keyboard.
* Click on a label and observe how focus moves.
* Mark fields as required and test browser validation.
* Navigate the form using only the Tab key.

---

## Key Principle to Remember

> If a screen reader cannot understand your form,
> many real users cannot use it either.

---

