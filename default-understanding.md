# 🧠 JavaScript — Optional Chaining (`?.`)

## 📌 Issue: Safely accessing deeply nested object properties

This snippet tests understanding of **optional chaining**, a syntax for safely accessing properties on potentially `null` or `undefined` objects.

---

## 🧪 Code Snippet

```javascript
const user = {
  name: 'Alice',
  address: {
    city: 'Denver'
  }
};

console.log(user.address?.city);       // Denver
console.log(user.contact?.phone);      // undefined
console.log(user.contact.phone);       // ❌ TypeError
```

⸻

✅ Output
```sh
Denver
undefined
TypeError: Cannot read properties of undefined (reading 'phone')
```

⸻

📖 Explanation
	•	user.address?.city accesses city only if address is not undefined or null.
	•	user.contact?.phone returns undefined without throwing.
	•	Accessing user.contact.phone directly throws a TypeError if contact is undefined.

⸻

💡 Use Case

Optional chaining is useful when:
	•	Accessing nested API response data
	•	Working with optional fields
	•	Avoiding defensive if checks

⸻

❓ Common Follow-Up Interview Questions
	1.	What does optional chaining replace?
Replaces verbose checks like:

if (user && user.contact && user.contact.phone)


	2.	Can you use optional chaining for function calls?
Yes:

user.sayHello?.()


	3.	What are the limitations?
Only works with undefined or null, not with other falsy values like '' or 0.

⸻
