# 🧠 JavaScript — Event Loop & Execution Order

## 📌 Issue: Microtasks vs Macrotasks in JavaScript

This snippet tests knowledge of the **JavaScript event loop**, particularly the difference between **Promise microtasks** and **setTimeout macrotasks**.

---

## 🧪 Code Snippet

```javascript
console.log('Start');

setTimeout(() => {
  console.log('Timeout');
}, 0);

Promise.resolve().then(() => {
  console.log('Promise');
});

console.log('End');
```

⸻

✅ Output
```javascript
Start
End
Promise
Timeout
```

⸻

📖 Explanation
	•	console.log('Start') runs immediately.
	•	setTimeout(..., 0) queues a macrotask.
	•	Promise.then(...) queues a microtask.
	•	Microtasks run before macrotasks — even if both are scheduled at the same time.

⸻

💡 Use Case

Understanding this order is critical for writing predictable async code, especially in UI rendering or scheduling logic.

⸻

❓ Common Follow-Up Interview Questions
	1.	What is the event loop?
It’s the mechanism that handles the execution of code, events, and queued tasks in JavaScript.
	2.	What’s the difference between microtasks and macrotasks?
Microtasks (e.g. Promises) run after the current stack but before any macrotasks (e.g. setTimeout, setInterval).
	3.	Why does Promise resolve before setTimeout?
Because Promise.then is a microtask and executes before the next event loop tick.

⸻


Let me know if you'd like the next one — such as `Array.prototype.map`, `reduce`, or prototype inheritance.