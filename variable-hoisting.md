# 🧠 JavaScript — Variable Hoisting

## 📌 Issue: Understanding Hoisting in JavaScript

This snippet checks the candidate’s knowledge of how JavaScript hoists `var`, `let`, and `const` declarations during the execution phase.

---

## 🧪 Code Snippet

```javascript
console.log(a); // undefined
var a = 10;

console.log(b); // ReferenceError
let b = 20;
```

---

## ✅ Output

```
undefined
ReferenceError: Cannot access 'b' before initialization
```

---

## 📖 Explanation

- **`var` is hoisted** to the top of its scope, but only the declaration — not the assignment.
- **`let` and `const` are also hoisted**, but they remain in a **temporal dead zone (TDZ)** until the line where they are defined.

---

## 💡 Use Case

Avoid using `var` in modern JavaScript. Use `let` for variables that will be reassigned, and `const` for constants.

---

## ❓ Common Follow-Up Interview Questions

1. **What is the Temporal Dead Zone (TDZ)?**
   - It's the phase between hoisting and declaration where a `let`/`const` variable exists but cannot be accessed.

2. **Is `var` function-scoped or block-scoped?**
   - Function-scoped.

3. **What’s the best practice for declaring variables in ES6+?**
   - Use `const` by default, and `let` when reassignment is required.

---
