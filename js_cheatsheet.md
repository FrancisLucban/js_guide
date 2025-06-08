# 🟦 1. Declaring Variables

```js
const name = "Alice"; // Constant (cannot be reassigned)
let age = 25; // Variable (can be reassigned)
// var (old, avoid using in modern JS)
```

# 🟦 2. Printing to Console

```js
console.log("Hello, world!");
```

> **_NOTE_**:
> must init node.js first to run

```
npm init -y
```

# 🟦 3. Data Types

```js
// String
const greeting = "Hi";

// Number
let score = 99;

// Boolean
const isOnline = true;

// Null
let empty = null;

// Undefined
let something;
```

# 🟦 4. Conditionals

### ➤ Standard

```js
if (score > 90) {
  console.log("Great job!");
} else if (score > 75) {
  console.log("Good effort!");
} else {
  console.log("Keep practicing!");
}
```

### ➤ One-Line Conditional

```js
condition ? true : false;
```

# 🟦 5. Comparison Operators

```js
===   // equal value & type
!==   // not equal value & type
>     // greater than
<     // less than
>=    // greater or equal
<=    // less or equal
```

# 🟦 6. Logical Operators

```js
&&  // and
||  // or
!   // not
```

# 🟦 7. Loops

### 🔁 For loop

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### 🔁 While loop

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

### 🔁 For...of (arrays)

```js
const fruits = ["apple", "banana", "cherry"];
for (const fruit of fruits) {
  console.log(fruit);
}
```

# 🟦 8. Functions

### ➤ Function Declaration

```js
function greet(name) {
  return "Hello, " + name;
}
```

### ➤ Arrow Function

```js
const greet = (name) => "Hello, " + name;
```

# 🟦 9. Arrays

```js
const colors = ["red", "green", "blue"];

colors.push("yellow"); // Add to end
colors.pop(); // Remove from end
colors.shift(); // Remove from start
colors.unshift("purple"); // Add to start

console.log(colors.length); // Get length
```

# 🟦 10. Strings

```js
const str = "JavaScript";

str.length; // Get length
str.toUpperCase(); // "JAVASCRIPT"
str.toLowerCase(); // "javascript"
str.includes("Script"); // true
str.indexOf("a"); // 1
str.slice(0, 4); // "Java"
str.split(""); // ["J","a","v",...]
```

# 🟦 11. Objects

```js
const user = {
  name: "Alice",
  age: 25,
  isAdmin: false,
};

console.log(user.name); // Access property
user.age = 30; // Update property
user.email = "a@b.com"; // Add new property
```

# 🟦 12. Typecasting

### 🔹 To String

| Method                  | Example            | Output  |
| ----------------------- | ------------------ | ------- |
| `String(value)`         | `String(123)`      | `"123"` |
| `value.toString()`      | `(123).toString()` | `"123"` |
| `"" + value` (implicit) | `"" + 123`         | `"123"` |

### 🔹 To Number

| Method                | Example                | Output   |
| --------------------- | ---------------------- | -------- |
| `Number(value)`       | `Number("123")`        | `123`    |
| `parseInt(value)`     | `parseInt("123px")`    | `123`    |
| `parseFloat(value)`   | `parseFloat("123.45")` | `123.45` |
| `+value` (unary plus) | `+"123"`               | `123`    |

### 🔹 To Boolean

| Method               | Example       | Output  |
| -------------------- | ------------- | ------- |
| `Boolean(value)`     | `Boolean("")` | `false` |
| `!!value` (double !) | `!!"hello"`   | `true`  |

### Example

```js
String(123); // "123"
(123).toString(); // "123"

Number("42"); // 42
parseFloat("3.14abc"); // 3.14
+"99"; // 99

Boolean(0); // false
!!"hello"; // true
```

# 🟦 12. Common Built-in Methods

| Category   | Method Example            | Description                                 |
| ---------- | ------------------------- | ------------------------------------------- |
| Type Check | `typeof "hello"`          | Returns the type (e.g., `"string"`)         |
| Array      | `array.push("x")`         | Add to end of array                         |
|            | `array.pop()`             | Remove from end                             |
|            | `array.shift()`           | Remove from start                           |
|            | `array.unshift("x")`      | Add to start                                |
|            | `array.includes("x")`     | Check if value exists in array              |
|            | `array.join(", ")`        | Join array elements into a string           |
|            | `array.reverse()`         | Reverse the array in place                  |
| String     | `"hi".toUpperCase()`      | → `"HI"` (convert to uppercase)             |
|            | `"HELLO".toLowerCase()`   | → `"hello"` (convert to lowercase)          |
|            | `"hello".slice(1, 3)`     | → `"el"` (substring from index 1 to 3)      |
|            | `"a,b,c".split(",")`      | → `["a", "b", "c"]` (split string to array) |
|            | `"hello".includes("ell")` | → `true` (check if substring exists)        |
| Math       | `Math.random()`           | Random number between 0 and 1               |
|            | `Math.floor(4.9)`         | Round down → `4`                            |
|            | `Math.ceil(4.1)`          | Round up → `5`                              |
|            | `Math.round(4.6)`         | Round to nearest → `5`                      |
|            | `Math.max(1, 2, 3)`       | Find max → `3`                              |
|            | `Math.min(1, 2, 3)`       | Find min → `1`                              |

# 13. Ternary Operator

```js
let weather = temperature > 25 ? `It's hot outside` : `The weather is nice`;

// if-else equivalent

if (temperature > 25) {
  console.log(`It's hot outside`);
} else {
  console.log(`The weather is nice`);
}
```

# 14. Optional Chaining

```js
const user = { profile: { name: "Francis" } };

console.log(user.profile?.name); // Francis
console.log(user.profile?.city); // undefined
```

Why use this technique? To avoid runtime errors when accessing deeply nested properties.

# 15. (IIFE) Immediately Invoked Function Expression

**Why do this?**

- It helps you keep things clean and private the stuff inside the function doesn't mess
  with the rest of your code.

```js
(function () {
  const message = `Hello, I'm batak!`;
  console.log(message);
})();
```

[IIFE MDN Reference](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)
