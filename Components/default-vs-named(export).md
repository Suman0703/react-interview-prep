# Default Export vs Named Export in React ⚛️
---

## 📌 Default Export

### What is Default Export?
A **default export** is used when a file exports **one main component**. We can only export one component from one file.

### Example
```jsx
function Button() {
  return <button>Click Me</button>;
}

export default Button;
```
---
## 📌 What is a Named Export?

A **named export** allows you to export a component, function, or variable
**by its specific name**. We can create multiple components in one file and we can export them using named export.

When importing, the name must **match exactly** with the exported name.

---

## 🧩 Example: Named Export Component

```jsx
export function Button() {
  return <button>Click Me</button>;
}
