from pathlib import Path

js_snippet_3 = """# 🧠 JavaScript Interview Code Snippet #3 — Closures

## 📌 Issue: Understanding Closures

This snippet tests a developer’s understanding of **closures**, where an inner function remembers the variables from its outer function scope even after the outer function has finished executing.

---

## 🧪 Code Snippet

```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();
counter(); // 1
counter(); // 2
counter(); // 3
```

---

## ✅ Output

```
1
2
3
```

---

## 📖 Explanation

- When `outer()` is called, it returns `inner()`, which forms a **closure** over the variable `count`.
- Even though `outer()` has finished executing, the returned `inner()` function **retains access** to the `count` variable in its lexical scope.

---

## 💡 Use Case

Closures are commonly used in:
- Data encapsulation
- Private variables
- Event handlers
- Functional programming patterns

---

## ❓ Common Follow-Up Interview Questions

1. **What is a closure?**
   - A closure is when a function retains access to its **lexical scope** even after the outer function has returned.

2. **Can you give a real-world use case for closures?**
   - Creating private variables in a factory function or module.

3. **What would happen if we used `var` instead of `let` in a loop with a closure?**
   - It can lead to unexpected behavior due to `var` being function-scoped instead of block-scoped.

---
"""

# Save to markdown file
file_path = Path("/mnt/data/js-interview-snippet-3.md")
file_path.write_text(js_snippet_3)

file_path.name