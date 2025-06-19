# 🧠 JavaScript — `this` Keyword Behavior

## 📌 Issue: Context Binding of `this`

This snippet tests the developer’s understanding of how `this` behaves differently depending on how a function is invoked.

---

## 🧪 Code Snippet

```javascript
const user = {
  name: 'Alice',
  greet() {
    console.log(`Hello, I am ${this.name}`);
  }
};

const greetFn = user.greet;
greetFn(); // undefined

const boundGreet = user.greet.bind(user);
boundGreet(); // Hello, I am Alice
```

⸻

✅ Output

```javascript
Hello, I am undefined
Hello, I am Alice
```

⸻

📖 Explanation
	•	When greetFn is assigned from user.greet, the function loses its original context (this is now undefined in strict mode or window in non-strict mode).
	•	Using .bind(user) creates a new function with this permanently bound to user, so it works as expected.

⸻

💡 Use Case

Bind is commonly used when passing class methods to callbacks (e.g., in React components, event handlers) to preserve context.

⸻

❓ Common Follow-Up Interview Questions
	1.	What are the 4 ways this can be set in JavaScript?
	•	Implicit (via object),
	•	Explicit (call, apply, bind),
	•	New binding (via new),
	•	Default/global (in strict/non-strict mode)
	2.	What does .bind() do?
	•	Returns a new function with this set to the provided object.
	3.	How does arrow function this behave?
	•	Arrow functions don’t have their own this, they inherit it from the enclosing lexical scope.

⸻