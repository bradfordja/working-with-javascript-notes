# 🧠 JavaScript — `==` vs `===` Comparison

## 📌 Issue: Type Coercion in Equality Check

JavaScript has two types of equality comparison: `==` (loose equality) and `===` (strict equality). This snippet tests a candidate’s understanding of **type coercion**.

---

## 🧪 Code Snippet

```javascript
console.log(0 == '0');   // true
console.log(0 === '0');  // false
```

---

## ✅ Output

```
true
false
```

---

## 📖 Explanation

- `0 == '0'`: JavaScript performs **type coercion**. It converts the string `'0'` to the number `0`, then compares them — so it returns `true`.
- `0 === '0'`: **Strict equality** checks both **type and value**. Here, one is a number and the other is a string — so it returns `false`.

---

## 💡 Use Case

Always prefer `===` to avoid bugs due to unexpected type coercion, especially in conditionals and API input validation.

---

## ❓ Common Follow-Up Interview Questions

1. **What’s the difference between `undefined` and `null`?**
   - `undefined`: Variable declared but not assigned.
   - `null`: Intentional absence of any value.

2. **What are falsy values in JavaScript?**
   - Values like `0`, `''`, `null`, `undefined`, `NaN`, and `false`.

3. **Why is type coercion dangerous in production code?**
   - It may lead to logic bugs if unexpected types are compared or passed around.

---
