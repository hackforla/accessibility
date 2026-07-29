
# ARIA Labels: `aria-label` or `aria-labelledby` or `aria-describedby`

## Overview

`aria-label`, `aria-labelledby`, and `aria-describedby` all improve accessibility, but they serve different purposes.

- **`aria-label`** gives an element an accessible **name** by explicitly defining the text.
- **`aria-labelledby`** gives an element an accessible **name** by referencing existing visible text.
- **`aria-describedby`** provides an accessible **description** with additional information that helps users understand or complete a specific control.

| Attribute | Purpose | Best Used When |
|-----------|---------|----------------|
| `aria-label` | Provides an accessible **name** by explicitly defining the text. | There is **no visible label** on the page (e.g., icon-only buttons). |
| `aria-labelledby` | Uses existing visible text as the accessible **name**. | There **is already visible text** that should serve as the label. |
| `aria-describedby` | Associates additional descriptive text with an element. | The element needs extra instructions, help text, or validation messages. |

---

# Example 1: Form Field (Native HTML - Best Practice)

### Visible Page

```
First Name

[_______________]
```

```html
<label for="firstName">
    First Name
</label>

<input
    id="firstName"
    type="text">
```

### Notes

This is the preferred approach. Native HTML automatically associates the label with the input, so **no ARIA is needed**.

If you're building a custom widget instead of using native HTML, `aria-labelledby` can provide the accessible name.

---

# Example 2: Icon-Only Button

There is no visible text.

```html
<button aria-label="Delete Project">
    🗑
</button>
```

### Screen Reader Announcement

```
Delete Project, button
```

### Why use `aria-label`?

Because there is no visible label for the button.

---

# Example 3: Using `aria-labelledby`

Suppose you have a project table.

```
Project Phoenix                 🗑
```

Instead of duplicating the text:

```html
<button aria-label="Delete Project Phoenix">
```

reference the existing text:

```html
<span id="projectName">
    Project Phoenix
</span>

<span id="deleteLabel" hidden>
    Delete
</span>

<button
    aria-labelledby="deleteLabel projectName">
    🗑
</button>
```

### Screen Reader Announcement

```
Delete Project Phoenix
```

### Why this is better

- No duplicate text
- If the project name changes, the accessible name changes automatically
- Keeps visible and accessible labels synchronized

---

# Example 4: Using `aria-describedby`

Visible page:

```
Password

[____________]

Must contain at least 12 characters.
```

```html
<label for="password">
    Password
</label>

<input
    id="password"
    type="password"
    aria-describedby="passwordHelp">

<p id="passwordHelp">
    Must contain at least 12 characters.
</p>
```

### Screen Reader Announcement

```
Password, edit text.
Must contain at least 12 characters.
```

Notice that:

- The **label** ("Password") is the accessible **name**.
- The help text is the accessible **description**.

---

# When NOT to Use `aria-describedby`

Suppose you have this form:

```
Name
Email
Address

We'll never share your contact details with anyone else.
```

Avoid this:

```html
<input aria-describedby="privacyNotice">
<input aria-describedby="privacyNotice">
<input aria-describedby="privacyNotice">
```

Every field would announce:

```
Name.
We'll never share your contact details with anyone else.

Email.
We'll never share your contact details with anyone else.

Address.
We'll never share your contact details with anyone else.
```

This becomes repetitive and does not help users complete each field.

Instead, leave the privacy notice as regular page content, or associate it with the form as a whole if it's essential context.

---

# `aria-label` vs. `aria-labelledby` vs. `aria-describedby`

## `aria-label`

You provide the accessible name yourself.

```html
<button aria-label="Delete Project">
```

### Advantages

- Simple
- Great for icon-only buttons
- No additional HTML required

### Disadvantages

- Can become outdated if visible text changes
- Creates duplicate content to maintain

---

## `aria-labelledby`

You reference existing visible text.

```html
<h2 id="title">
    Delete Project
</h2>

<div
    role="dialog"
    aria-labelledby="title">
```

### Advantages

- Uses the visible text
- Keeps visual and accessible labels synchronized
- Preferred whenever a visible label already exists

### Disadvantages

- Requires the referenced element to exist
- Slightly more setup than `aria-label`

---

## `aria-describedby`

You reference existing descriptive text.

```html
<input
    aria-describedby="passwordHelp">
```

### Advantages

- Provides additional instructions
- Excellent for help text and validation messages
- Keeps descriptions separate from accessible names

### Disadvantages

- Should not be used for general page information
- Can become repetitive if applied unnecessarily to many controls

---

# Rule of Thumb

| Situation | Recommended Approach |
|-----------|----------------------|
| Native form input | Use a native `<label>` |
| Icon-only button | `aria-label` |
| Visible label already exists | `aria-labelledby` |
| Dialog or modal title | `aria-labelledby` |
| Region with visible heading | `aria-labelledby` |
| Additional instructions for one control | `aria-describedby` |
| Password requirements | `aria-describedby` |
| Validation or error messages | `aria-describedby` |
| General page information or privacy notices | Usually **do not** use `aria-describedby` |

---

# Easy Way to Remember

### `aria-label`

> **"Here's the name."**

You provide the name yourself.

---

### `aria-labelledby`

> **"That text over there is the name."**

You point to existing visible text.

---

### `aria-describedby`

> **"Here's some extra information."**

You point to additional text that helps the user understand or complete a specific control.

---

# Summary

- Use native HTML (`<label>`) whenever possible.
- Use **`aria-labelledby`** whenever a visible label already exists.
- Use **`aria-label`** only when no visible label is available.
- Use **`aria-describedby`** only for instructions, help text, or validation messages that are relevant to a specific control.
- Avoid using `aria-describedby` for general page information, such as privacy notices or explanatory text that applies to the entire page.
- Keeping visible text and accessible names synchronized improves accessibility and maintainability.

---

- Page Status: Complete
- Current Authors: 
    - Bonnie Wolfe
    - Rabia Shaikh
