# 🎨 Introduction to CSS

## 🔍 CSS Selectors

### 🔹 Universal Selector (`*`)

Applies to all elements.

```css
* {
  color: purple;
}
```

### 🔹 Type Selector

Targets specific HTML tags.

```css
div {
  background-color: black;
}
```

### 🔹 Class Selector (`.`)

Targets all elements with a class.

```html
<div class="alert-text">...</div>
```

```css
.alert-text {
  color: red;
}
```

### 🔹 ID Selector (`#`)

Targets a unique element with an ID.

```html
<div id="title">My Page</div>
```

```css
#title {
  background-color: red;
}
```

---

## 🧵 Combining Selectors

### 🔸 Grouping Selectors (`,`)

Apply same rules to multiple selectors.

```css
.read,
.unread {
  color: white;
  background-color: black;
}
```

### 🔸 Chaining Selectors (no space)

Targets elements that match all chained selectors.

```html
<div class="subsection header">Latest</div>
```

```css
.subsection.header {
  color: red;
}
```

You can also chain with IDs:

```css
.subsection#preview {
  color: blue;
}
```

---

## 📐 Descendant Combinator (` `)

Selects elements _inside_ other elements.

```css
.ancestor .child {
  color: green;
}
```

Only elements with class `child` **inside** `.ancestor` will be affected.

---
