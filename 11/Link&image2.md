# 📚 HTML: Links and Images

## 🔗 Links

### ✅ Anchor Tag

```html
<a href="https://example.com">Visit Example</a>
```

### 📌 Attributes

- `href`: Specifies the URL
- `target="_blank"`: Opens link in a new tab
- `rel="noopener noreferrer"`: Security and privacy (prevents tabnabbing)

**Example:**

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer"
  >Open in New Tab</a
>
```

## 🖼️ Images

### ✅ Image Tag

```html
<img src="images/dog.jpg" alt="A happy dog" width="300" height="200" />
```

### 📌 Required Attributes

- `src`: Image path (relative or absolute)
- `alt`: Describes the image for accessibility

### ✅ Recommended

- `width` and `height`: Prevent layout shifts
