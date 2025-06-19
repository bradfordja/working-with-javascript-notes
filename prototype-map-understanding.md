# 🧠 JavaScript — `map()` vs `forEach()`

## 📌 Issue: Understanding the difference between `.map()` and `.forEach()`

This snippet evaluates whether a developer understands **array transformation vs iteration** using `map()` and `forEach()`.

---

## 🧪 Code Snippet

```javascript
const numbers = [1, 2, 3];

const doubled = numbers.map(n => n * 2);
console.log('map result:', doubled);

const results = [];
numbers.forEach(n => results.push(n * 2));
console.log('forEach result:', results);
```

⸻

✅ Output
```sh
map result: [2, 4, 6]
forEach result: [2, 4, 6]
```

⸻

📖 Explanation
	•	.map() creates a new array by applying a function to each element. It’s pure and chainable.
	•	.forEach() is used for side effects. It does not return a new array — you must manage results manually.

⸻

💡 Use Case
	•	Use .map() when you need a new transformed array.
	•	Use .forEach() when performing side effects like logging, DOM updates, or mutation.

⸻

❓ Common Follow-Up Interview Questions
	1.	Can .map() be used instead of .forEach()?
Only if you need to return and use the new array.
	2.	What does .map() return if you don’t return anything in the callback?
An array of undefined.
	3.	Is .forEach() asynchronous?
No, both .map() and .forEach() are synchronous.

⸻