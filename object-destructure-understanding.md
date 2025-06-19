# 🧠 JavaScript — Object Destructuring

## 📌 Issue: Extracting values from objects using destructuring syntax

This snippet tests whether a developer understands **object destructuring**, a powerful ES6 feature for cleaner and more readable code.

---

## 🧪 Code Snippet

```javascript
const user = {
  id: 101,
  name: 'Alice',
  location: {
    city: 'Denver',
    state: 'CO'
  }
};

const { name, location: { city } } = user;

console.log(name); // Alice
console.log(city); // Denver
```

⸻

✅ Output
```sh
Alice
Denver
```

⸻

📖 Explanation
	•	The destructuring syntax extracts properties from objects and assigns them to variables.
	•	You can deeply destructure nested objects, like extracting city from location.

⸻

💡 Use Case

Object destructuring simplifies:
	•	Accessing nested API response data
	•	Passing props in React
	•	Cleaner variable declarations

⸻

❓ Common Follow-Up Interview Questions
	1.	Can you rename a property while destructuring?
Yes:

```javascript
const { name: fullName } = user;
```

	2.	Can you set default values in destructuring?
Yes:
```javascript
const { age = 30 } = user;
```

	3.	Can you destructure arrays too?
Absolutely — that’s called array destructuring.

⸻


Let me know if you want the next snippet on prototype inheritance, spread/rest operators, or module imports/exports.