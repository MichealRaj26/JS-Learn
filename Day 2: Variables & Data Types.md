# Day 2: Variables & Data Types

## Variables in JavaScript
Variables are used to **store data** in JavaScript. They allow us to store and manipulate values dynamically.

### Declaring Variables
JavaScript provides three ways to declare variables:
1. **var** (function-scoped, can be redeclared)
2. **let** (block-scoped, cannot be redeclared in the same scope)
3. **const** (block-scoped, cannot be reassigned)

### `var` Example (Function Scope)
```js
var name = "Alice";
console.log(name); // Output: Alice

var name = "Bob"; // Redeclaration allowed
console.log(name); // Output: Bob
```

### `let` Example (Block Scope)
```js
let age = 25;
console.log(age); // Output: 25

age = 30; // Allowed
console.log(age); // Output: 30

// let age = 40; // ❌ Error: Cannot redeclare a let variable in the same scope
```

### `const` Example (Constant Value)
```js
const country = "USA";
console.log(country); // Output: USA

// country = "Canada"; // ❌ Error: Assignment to constant variable
```

### Real-World Example:
**Scenario:** Consider an e-commerce website where we need to store product details.
```js
const productName = "Laptop"; // Constant because the name does not change
let price = 1000; // Can change if there's a discount
var stock = 50; // Stock might be updated globally

console.log(`Product: ${productName}, Price: $${price}, Stock: ${stock}`);
```

---

## Primitive Data Types
JavaScript has **7 primitive data types**:
1. **String** - Represents text values.
2. **Number** - Represents both integer and floating-point numbers.
3. **Boolean** - Represents `true` or `false`.
4. **Null** - Represents an **intentional absence of value**.
5. **Undefined** - Represents an **uninitialized variable**.
6. **Symbol** - Represents unique values (used in advanced cases).
7. **BigInt** - Represents large integers beyond `Number` limits.

### String Example
```js
let firstName = "John";
let lastName = 'Doe';
console.log(firstName + " " + lastName); // Output: John Doe
```

### Number Example
```js
let age = 30;
let price = 99.99;
console.log(age, price); // Output: 30 99.99
```

### Boolean Example
```js
let isMember = true;
let hasDiscount = false;
console.log(isMember, hasDiscount); // Output: true false
```

### Null Example
```js
let address = null;
console.log(address); // Output: null
```

### Undefined Example
```js
let city;
console.log(city); // Output: undefined
```

### Real-World Example:
**Scenario:** Checking if a user is logged in on a website.
```js
let userName = "Mike"; // String
let isLoggedIn = true; // Boolean
let sessionTimeout = null; // Null (until assigned a value)

console.log(`User: ${userName}, Logged In: ${isLoggedIn}, Timeout: ${sessionTimeout}`);
```

---

## Type Conversion
JavaScript allows conversion between different data types.

### Converting to Number
- `parseInt()` - Converts a string to an integer.
- `parseFloat()` - Converts a string to a floating-point number.
- `Number()` - Converts a value to a number.

```js
let strNum = "42";
console.log(parseInt(strNum)); // Output: 42
console.log(parseFloat("42.5")); // Output: 42.5
console.log(Number("10")); // Output: 10
```

### Converting to String
```js
let num = 100;
console.log(String(num)); // Output: "100"
console.log(num.toString()); // Output: "100"
```

### Converting to Boolean
```js
console.log(Boolean(0)); // Output: false
console.log(Boolean(1)); // Output: true
console.log(Boolean("")); // Output: false
console.log(Boolean("Hello")); // Output: true
```

### Real-World Example:
**Scenario:** Handling user input from a form (converting input values).
```js
let inputAge = "25"; // User enters as string
let numericAge = Number(inputAge);
console.log(numericAge + 5); // Output: 30
```

---

## `typeof` Operator
The `typeof` operator returns the **data type** of a value.

### Example Usage
```js
console.log(typeof "Hello"); // Output: string
console.log(typeof 42); // Output: number
console.log(typeof true); // Output: boolean
console.log(typeof null); // Output: object (a known JavaScript quirk)
console.log(typeof undefined); // Output: undefined
```

### Real-World Example:
**Scenario:** Validating user input type in a form.
```js
function checkInput(value) {
    if (typeof value === "number") {
        console.log("Valid Number Input");
    } else {
        console.log("Invalid Input, please enter a number");
    }
}
checkInput(25); // Output: Valid Number Input
checkInput("Hello"); // Output: Invalid Input, please enter a number
```

---

## Summary of Day 2
| Topic                        | Key Takeaways |
|------------------------------|--------------|
| **var, let, const**          | Different ways to declare variables. Use `let` and `const` instead of `var`. |
| **Primitive Data Types**     | String, Number, Boolean, Null, Undefined, Symbol, BigInt. |
| **Type Conversion**          | Use `parseInt()`, `parseFloat()`, `Number()`, `String()`, `Boolean()` for conversions. |
| **typeof Operator**          | Used to check the data type of a variable. |

---

Now that you understand variables and data types, you are ready to explore **operators and expressions** on Day 3! 🚀
