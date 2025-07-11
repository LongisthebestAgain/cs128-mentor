# The CSS Box Model

### What is the Box Model?

Every element on a webpage is a rectangular box made up of:

- **Content** — The text, images, or other content inside the element.
- **Padding** — Space between the content and the border.
- **Border** — The line surrounding the padding.
- **Margin** — Space outside the border, separating the element from other elements.

---

### Visual Example of Box Model Parts

```css
.box {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  margin: 15px;
  background-color: lightblue;
}
```

```html
<div class="box">This is a box model example.</div>
```

- **Content area:** 200px wide
- **Padding:** adds 20px on all sides inside the border
- **Border:** 5px thick around padding
- **Margin:** 15px space outside the border

---

### How Width and Height Work by Default (`content-box`)

- The `width` and `height` properties apply **only to the content area**.
- Padding and border add extra size outside the content size.

For example, total width = content width + padding (left + right) + border (left + right)

Using the example above:
Total width = 200 + 20*2 + 5*2 = 250px total width visually on the page.

---

### Using `box-sizing: border-box`

This changes the box model calculation so that:

- The specified `width` and `height` include content, padding, and border.
- This makes it easier to size elements without worrying about padding/border adding extra size.

Example:

```css
.box {
  box-sizing: border-box;
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  margin: 15px;
  background-color: lightgreen;
}
```

Here, the **total width** remains 200px — padding and border are included inside the 200px.

---

### What Do Margin, Padding, and Border Do?

| Property | Description                                | Effect                                      |
| -------- | ------------------------------------------ | ------------------------------------------- |
| Margin   | Space outside the border, between elements | Pushes elements apart                       |
| Border   | A line surrounding the element             | Visually separates content and surroundings |
| Padding  | Space between content and border           | Adds breathing room inside the box          |

---

### Quick Tips

- Use **margin** to create space between elements.
- Use **padding** to create space between content and its border.
- Use `box-sizing: border-box` to keep sizing intuitive.

---

### Centering an Element Horizontally

A common use of margin is centering:

```css
.centered {
  width: 300px;
  margin: 0 auto; /* top/bottom margin 0, left/right margin auto */
  border: 1px solid gray;
  padding: 10px;
}
```

```html
<div class="centered">Centered box</div>
```

This centers the box horizontally inside its container.
