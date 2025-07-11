**CSS Cascade **

1. **What is the Cascade?**
   The cascade decides which CSS rule applies when multiple rules target the same element. It helps resolve conflicts between styles.

2. **Specificity Ranking (from highest to lowest):**

   - Inline styles (e.g., `style="..."`)
   - ID selectors (e.g., `#id`)
   - Class selectors (e.g., `.class`)
   - Type selectors (e.g., `div`, `p`)

3. **Examples of Specificity:**

   - `#header` beats `.menu`
   - `.main .list` (two classes) beats `.list` (one class)
   - Inline style beats any selector

4. **What Does NOT Add Specificity:**

   - Universal selector (`*`)
   - Combinators (`>`, `+`, `~`, space)

5. **Inheritance:**
   Some properties like `color`, `font-family`, and `font-size` are automatically passed down to child elements.
   If a child has its own rule for that property, it overrides the inherited one.

6. **Rule Order:**
   If two rules have the same specificity, the one declared **last** in the CSS file wins.

---

**Quick Examples:**

- **ID beats Class:**

```css
#id {
  color: blue;
}
.class {
  color: red;
}
```

Text will be blue on an element with both `id` and `class`.

- **Multiple Classes vs Single Class:**

```css
.main .list {
  color: red;
}
.list {
  color: blue;
}
```

Text will be red inside `<div class="main list">`.

- **Inheritance:**

```css
#parent {
  color: red;
}
.child {
  /* no color set */
}
```

Text inside `.child` will be red because of inheritance.

- **Override Inheritance:**

```css
.child {
  color: blue;
}
```

Now `.child` text is blue, overriding inherited red.

- **Rule Order Wins Tie:**

```css
.alert {
  color: red;
}
.warning {
  color: yellow;
}
```
