# 🧠 JavaScript — Prototype Inheritance

## 📌 Issue: Understanding JavaScript's prototype chain

This snippet tests whether a developer understands how JavaScript uses **prototypal inheritance** instead of classical inheritance.

---

## 🧪 Code Snippet

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.sayHello = function() {
  return `Hello, I'm ${this.name}`;
};

const alice = new Person('Alice');

console.log(alice.sayHello());
console.log(alice.__proto__ === Person.prototype); // true
```

⸻

✅ Output
```sh
Hello, I'm Alice
true
```

⸻

📖 Explanation
	•	Person is a constructor function.
	•	sayHello() is added to Person.prototype, so all instances share it.
	•	alice.__proto__ points to Person.prototype, forming the prototype chain.

⸻

💡 Use Case

Prototype inheritance allows shared methods and properties across all instances, saving memory and following DRY principles.

⸻

❓ Common Follow-Up Interview Questions
	1.	What is the difference between __proto__ and prototype?
	•	prototype is a property on constructor functions.
	•	__proto__ is the actual reference chain used by instances.
	2.	How is class-based inheritance implemented in ES6?
Using class and extends, which is syntactic sugar over prototype inheritance.
	3.	Can you override inherited methods?
Yes, by redefining the method directly on the instance or subclass prototype.

⸻
