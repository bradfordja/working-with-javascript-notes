# 🧠 JavaScript — `Array.prototype.reduce()`

## 📌 Issue: Using `reduce()` to aggregate or transform data

This snippet evaluates understanding of the `reduce()` method to perform **accumulation logic**, like summing or restructuring arrays.

---

## 🧪 Code Snippet

```javascript
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((acc, curr) => acc + curr, 0);

console.log('Sum:', sum);
```

⸻

✅ Output
```sh
Sum: 15
```

⸻

📖 Explanation
	•	reduce() takes a callback function with an accumulator and the current value.
	•	The initial value is 0.
	•	It adds each number to the accumulator and returns the total.

⸻

💡 Use Case

reduce() is perfect for:
	•	Summing values
	•	Grouping data
	•	Flattening arrays
	•	Transforming arrays into objects

⸻

❓ Common Follow-Up Interview Questions
	1.	What are the arguments passed to the reduce() callback?
	•	accumulator, currentValue, currentIndex, array
	2.	Can reduce() return a different data type than the input array?
	•	Yes, it can return a number, object, string, etc.
	3.	What happens if you omit the initial value?
	•	The first array element is used as the initial accumulator, and iteration starts from the second element.

⸻


Let me know if you'd like the next snippet on object destructuring, prototype inheritance, or spreading/rest parameters.