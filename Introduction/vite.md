# ⚡ What is Vite and Why Do We Use It?

Vite (pronounced **“veet”**, meaning *fast* in French) is a **modern frontend build tool**
used to develop web applications **quickly and efficiently**, especially with frameworks
like **React, Vue, and Svelte**.

This document explains **what Vite is**, **how it works internally**, and **why developers prefer it**.

---

## 📌 What is Vite?

**Vite is a development and build tool** that helps you:
- Run your project during development
- See changes instantly
- Create optimized files for production

In short:
> **Vite makes frontend development faster and smoother.**

---

## 🚨 Problem with Older Tools

Before Vite, tools like **Webpack / Create React App (CRA)** worked by:
- Bundling **all files** before starting the app
- Rebuilding large parts of the app on every change

### ❌ Result:
- Slow startup time
- Slow refresh
- Poor developer experience

---

## 🚀 How Vite Works (Simple but Deep)

Vite works **differently in development and production**.

---

### 🔹 1. Development Mode (Key Feature)

During development, Vite:
- Uses **native ES Modules** (a browser feature)
- **Does NOT bundle the entire app**
- Loads files **only when they are needed**

#### Example:
```js
import Header from './Header.jsx'
