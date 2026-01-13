# State in React & Its Relation with Hooks

## 📌 What is State in React?

**State** in React is a built-in object that is used to **store and manage data that can change over time**.

When state changes, **React automatically re-renders the component** to reflect the updated data on the UI.

👉 In simple words:

> **State = Component’s memory**

---

## 🧠 Why Do We Need State?

Normal JavaScript variables **cannot update the UI automatically** when their value changes.

State solves this problem by:

* Tracking dynamic data
* Updating the UI when data changes
* Keeping the UI and data in sync

### ❌ Without State

```js
let count = 0;
count = count + 1;
// UI will NOT update
```

### ✅ With State

```js
const [count, setCount] = useState(0);
setCount(count + 1);
// UI updates automatically
```

---

## 🛠 What Kind of Data is Stored in State?

State is used for **dynamic and interactive data**, such as:

* Form inputs
* Button clicks count
* Toggle (dark/light mode)
* API response data
* Login/logout status
* Show/hide components

---

## 🔄 How State Works (Behind the Scenes)

1. Component renders for the first time
2. State is initialized
3. User interacts with UI
4. State changes using setter function
5. React re-renders the component
6. Updated UI is shown

---

## ⚙️ What Are Hooks in React?

**Hooks** are special functions introduced in React **16.8** that allow you to:

* Use state in functional components
* Use lifecycle features without class components

👉 Hooks make React code **simpler, cleaner, and reusable**.

---

## 🔗 Relationship Between State and Hooks

Before hooks, **state was only available in class components**.

Hooks introduced state into **functional components**.

### 🔑 Key Relationship

> **State is managed using Hooks** in functional components

The most important hook for state is:

### 🪝 `useState` Hook

```js
import { useState } from 'react';

const [value, setValue] = useState(initialValue);
```

* `value` → current state
* `setValue` → function to update state
* `initialValue` → starting value of state

---

## 🧩 Example: Counter Using State & Hook

```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>+</button>
    </div>
  );
}
```

---

## 🔁 State Update is Asynchronous

React does **not update state immediately**.

```js
setCount(count + 1);
console.log(count); // old value
```

To update based on previous state:

```js
setCount(prev => prev + 1);
```

---

## 🚫 Rules of State & Hooks

1. Hooks must be called **at the top level**
2. Hooks cannot be called inside loops or conditions
3. State should **never be modified directly**

❌ Wrong

```js
count = count + 1;
```

✅ Correct

```js
setCount(count + 1);
```

---

## 🆚 Props vs State

| Props              | State                    |
| ------------------ | ------------------------ |
| Passed from parent | Managed inside component |
| Read-only          | Can be changed           |
| Immutable          | Mutable via setter       |

---

## 📌 When Should You Use State?

Use state when:

* Data changes over time
* UI depends on user interaction
* You need re-rendering

Do NOT use state for:

* Static values
* Constants
* Calculations that don’t affect UI

---

## 📎 Summary

| Concept   | Explanation               |
| --------- | ------------------------- |
| State     | Stores dynamic data       |
| Purpose   | Updates UI automatically  |
| Hook Used | `useState()`              |
| Trigger   | User interaction / events |
| Benefit   | Reactive UI               |

---

## 🏁 Final Note

State is the **heart of React’s reactivity**.

Hooks make state:

* Easier to use
* Cleaner to manage
* Reusable across components

Mastering state + hooks means mastering React 🚀
