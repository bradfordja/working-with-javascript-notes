# 🧠 JavaScript — Spread and Rest Operators

## 📌 Issue: Understanding `...` in different contexts

This snippet tests whether a developer understands the dual use of the `...` syntax for **expanding** (spread) and **collecting** (rest).

---

## 🧪 Code Snippet

```javascript
// Spread
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
console.log('Spread:', arr2);

// Rest
function sum(...numbers) {
  return numbers.reduce((acc, n) => acc + n, 0);
}
console.log('Rest sum:', sum(1, 2, 3));
```

⸻

✅ Output
```sh
Spread: [1, 2, 3, 4]
Rest sum: 6
```

⸻

📖 Explanation
	•	Spread expands an iterable (like an array or object) into individual elements.
	•	Rest collects remaining arguments into an array for functions.

⸻

💡 Use Case
	•	Use spread for combining arrays or cloning objects.
	•	Use rest to write flexible functions like logging or summing inputs.

⸻

❓ Common Follow-Up Interview Questions
	1.	Can you use spread with objects?
Yes:

const obj = { a: 1, b: 2 };
const newObj = { ...obj, c: 3 };


	2.	Can rest and spread be used together?
Yes — rest in function parameters, spread in arguments:

sum(...[1, 2, 3]);


	3.	What happens if spread is used on a non-iterable?
It throws an error — only iterables (like arrays, strings) can be spread.

⸻


Let me know if you’d like the next one on optional chaining (`?.`), nullish coalescing (`??`), or ES module imports/exports.