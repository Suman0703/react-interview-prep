# 📦 ES Modules (ECMAScript Modules)

ES Modules, also known as **ECMAScript Modules (ESM)**, are the **official JavaScript module system**
introduced in **ES6 (2015)**.  
They allow developers to split JavaScript code into **reusable, maintainable, and organized files**.

---

## 📌 Full Form

**ES Modules = ECMAScript Modules**

---

## 🤔 Why ES Modules Were Introduced

Before ES Modules:
- JavaScript code was often written in one large file
- Global variables caused conflicts
- Code was hard to maintain and scale

ES Modules solved these problems by introducing:
- File-based modular structure
- Clean import/export syntax
- Better performance and organization

---

## 🔁 How ES Modules Work

Each JavaScript file is treated as a **module**.

### 📤 Exporting Code
```js
// math.js
export function add(a, b) {
  return a + b
}
```
---

### 📥 Importing Code
```js
// main.js
import { add } from './math.js'

console.log(add(2, 3))
