# React Hooks

## 📌 What are Hooks in React?

**Hooks** are special functions in React that allow you to **use React features (like state, lifecycle methods, context, etc.) inside functional components**.

Hooks were introduced in **React 16.8** to make React components:

* Simpler
* Cleaner
* More reusable

👉 In simple words:

> **Hooks let functional components do everything that class components could do** (and more).

---

## ❓ Why Were Hooks Introduced? (Need of Hooks)

Before Hooks, React had two main problems:

### 1️⃣ Complex Class Components

* Required `this` keyword
* Confusing lifecycle methods
* Hard for beginners

```js
class Counter extends React.Component {
  constructor() {
    super();
    this.state = { count: 0 };
  }
}
```

---

### 2️⃣ Code Reusability Issues

* Logic reuse was difficult
* Used patterns like HOCs and Render Props
* Code became messy and hard to understand

---

### ✅ Hooks Solve These Problems

Hooks allow:

* Using state in functional components
* Sharing logic easily
* Writing less code
* Avoiding `this`

---

## ⚙️ What Can Hooks Do?

Using hooks, we can:

* Manage state
* Handle lifecycle events
* Access context
* Work with refs
* Optimize performance

All **without using class components**.

---

## 🪝 Commonly Used React Hooks

### 1️⃣ `useState`

Used to manage state in functional components.

```js
const [count, setCount] = useState(0);
```

---

### 2️⃣ `useEffect`

Used to handle side effects (API calls, subscriptions, DOM updates).

```js
useEffect(() => {
  console.log("Component mounted");
}, []);
```

---

### 3️⃣ `useContext`

Used to access context without prop drilling.

```js
const value = useContext(MyContext);
```

---

### 4️⃣ `useRef`

Used to access DOM elements or persist values without re-rendering.

```js
const inputRef = useRef();
```

---

### 5️⃣ `useMemo`

Used to memoize expensive calculations.

```js
const result = useMemo(() => calculate(a), [a]);
```

---

### 6️⃣ `useCallback`

Used to memoize functions.

```js
const handleClick = useCallback(() => {}, []);
```

---

## ✨ Features of React Hooks

### ⭐ 1. Simpler Code

* No class syntax
* No `this` keyword
* Less boilerplate

---

### ⭐ 2. Better Readability

* Logic grouped by feature
* Easy to understand and maintain

---

### ⭐ 3. Reusability

* Custom hooks allow sharing logic

```js
function useCounter() {
  const [count, setCount] = useState(0);
  return { count, setCount };
}
```

---

### ⭐ 4. Functional Programming Style

* Encourages clean and predictable code
* Easier testing

---

### ⭐ 5. No Breaking Changes

* Hooks work alongside class components
* Old code still works

---

## 🚫 Rules of Hooks

1. Hooks must be called at the **top level**
2. Do not call hooks inside loops or conditions
3. Hooks must be called inside React components or custom hooks

---

## 🆚 Hooks vs Class Components

| Hooks         | Class Components |
| ------------- | ---------------- |
| Simple syntax | Complex syntax   |
| No `this`     | Uses `this`      |
| Easy reuse    | Hard reuse       |
| Recommended   | Legacy approach  |

---

## 📌 When Should You Use Hooks?

Use hooks when:

* Building new React applications
* Writing functional components
* Want clean and modern React code

Avoid hooks only if:

* Working with very old React versions

---

## 📎 Summary

| Topic      | Explanation                       |
| ---------- | --------------------------------- |
| Hooks      | Functions that add React features |
| Purpose    | Replace class components          |
| Introduced | React 16.8                        |
| Benefits   | Clean, reusable, readable code    |
| Future     | Official React standard           |

---

## 🏁 Final Note

Hooks are one of the **most important features of modern React**.

If you master hooks, you master:

* State management
* Lifecycle handling
* Code reusability

👉 **Hooks = Modern React Development** 🚀
