# **CSS-Cheatsheet**

## 1. **CSS Basics**

### **Linking CSS**

```html
<link rel="stylesheet" href="styles.css" />
```

> Place this inside the <head> section of your HTML document.

### **Universal Reset**

```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

---

## 2. **CSS Positioning**

### relative

- Positioned reative to its original position.
- Useful as a container for absolutely positioned child elements.

### absolute

- Removed from the normal document flow.
- Positioned relative to the nearest positioned ancestor (non-static).
- If no parent is positioned -> relative to html tag

### relative + absolute combo

```css
.parent {
  position: relative;
}
.child {
  position: absolute;
}
```

### sticky

- Acts like relative until a certain scroll point, then "sticks" - useful to stick headings below the navigation bar when having long sections, e.g. book chapters.

```css
position: sticky;
top: 15px;
```

### fixed

- Positioned relative to the **viewport**, not the document.
- Stays visible and fixed when scrolling.
- Common use cases: headers/navigation bars, floating "Back to top" buttons.
- Remember to adjust **z-index** and **body padding** if needed.

---

## CSS Flexbox

- Great for 1D layouts (row or column).

```css
display: flex; /*Default direction: row*/
```

### Common properties

```css
flex-direction: row | column;
flex-wrap: wrap; /* for responsive layout */
justify-content: center; /* alignment along main axis */
align-items: center; /* alignment along cross axis */
```

> Use case: Horizontal navigation bars (html ul tag as a flex container).

---

## CSS Grid

- Perfect for 2D layouts (rows + columns).

```css
display: grid;
grid-template-columns: repeat(3, 1fr);
grid-gap: 1rem;
```

### Flex vs. Grid

| Feature          |      Flexbox       |                Grid |
| ---------------- | :----------------: | ------------------: |
| Layout direction | 1D (row or column) | 2D (rows + columns) |
| Typical use      |   Navbars, cards   |     Complex layouts |

---

## CSS Structure

### Cascade

- Styles apply from top to bottom.
- If specificity is equal, the last defined rule wins.

### Specificity Hierarchy

| Selector Type        | Value |            Example |
| -------------------- | :---- | -----------------: |
| Inline Styles        | 1000  | `<div style="..."` |
| ID Selector          | 100   |            #header |
| Class / Pseudo-class | 10    |      .button:hover |
| Element Selector     | 1     |              p, h1 |

### BEM Method

Keeps class names **structured** and **readable**.

```css
.block__element--modifier {
  ...;
}
```

### CSS Variables

```css
:root {
  --primary: #123456;
  --secondary: #abcdef;
}
```

---

## Responsive Design

Mobile-First Approach

- Better for performance and scalability.
- Start with base styles for small screens, then expand with min-width.

### Example

```css
@media (min-width: 768px) {
  body {
    font-size: 1.2 rem;
  }
}
```

---

## Pro Tip

Start with **semantic HTML** and **mobile-first CSS**, then enhance with **positioning**, **flex/grid layouts**, and keep your CSS **clean and maintainable** using **variables** and **BEM**.
