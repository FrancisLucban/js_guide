# 🟦 1. Declaring Variables
```js
const name = "Alice";     // Constant (cannot be reassigned)
let age = 25;             // Variable (can be reassigned)
// var (old, avoid using in modern JS)
```

# 🟦 2. Printing to Console
```js
console.log("Hello, world!");
```
> **_NOTE_**:
must init node.js first to run
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

# 🟦 7. Special Operators
| Operator        | Name                        | Description / Example                                                                 |
|-----------------|-----------------------------|----------------------------------------------------------------------------------------|
| `...`           | Spread / Rest               | Spread: `f(...arr)` unpacks array. Rest: `function(...args)` gathers remaining args   |
| `typeof`        | Typeof                      | Returns the type: `typeof 42` → `"number"`                                            |
| `instanceof`    | Instanceof                  | Checks constructor: `obj instanceof Array` → `true`                                   |
| `in`            | Property checker            | Checks if a key exists in an object: `'x' in obj`                                     |
| `??`            | Nullish coalescing          | `a ?? b`: returns `a` if not `null`/`undefined`, otherwise `b`                        |
| `?.`            | Optional chaining           | Safe nested access: `obj?.user?.name`                                                 |
| `==` / `===`    | Equality / Strict equality  | `==` allows coercion, `===` checks type and value                                     |
| `!=` / `!==`    | Inequality / Strict inequality | Opposite of `==` / `===`                                                            |
| `=>`            | Arrow function              | Short function syntax: `const fn = x => x * 2`                                        |
| `!!`            | Double negation             | Converts to boolean: `!!"text"` → `true`                                              |
| `delete`        | Delete property             | Removes a property: `delete obj.key`                                                 |
| `new`           | Object instantiation        | Creates object: `new Date()`                                                         |
| `await`         | Await                       | Waits for promise: `await fetch(url)` (inside `async` function)                      |
| `void`          | Void                        | Evaluates an expression and returns `undefined`: `void 0`                             |

### 🧠 Notes on the ... Operator:
**Spread (for unpacking):**
```js
const arr = [1, 2, 3];
console.log(...arr); // 1 2 3
```

**Rest (for gathering):**
```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b);
}
sum(1, 2, 3); // 6
```

# 🟦 8. Loops
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

# 🟦 9. Functions
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

# 🟦 10. Arrays
```js
const colors = ["red", "green", "blue"];

colors.push("yellow");       // Add to end
colors.pop();                // Remove from end
colors.shift();              // Remove from start
colors.unshift("purple");    // Add to start

console.log(colors.length);  // Get length
```

# 🟦 11. Strings
```js
const str = "JavaScript";

str.length;              // Get length
str.toUpperCase();       // "JAVASCRIPT"
str.toLowerCase();       // "javascript"
str.includes("Script");  // true
str.indexOf("a");        // 1
str.slice(0, 4);         // "Java"
str.split("");           // ["J","a","v",...]
```

# 🟦 12. Objects
```js
const user = {
    name: "Alice",
    age: 25,
    isAdmin: false
};

console.log(user.name);        // Access property
user.age = 30;                 // Update property
user.email = "a@b.com";        // Add new property
```

# 🟦 13. Typecasting

### 🔹 To String
| Method                  | Example             | Output   |
|-------------------------|---------------------|----------|
| `String(value)`         | `String(123)`       | `"123"`  |
| `value.toString()`      | `(123).toString()`  | `"123"`  |
| `"" + value` (implicit) | `"" + 123`          | `"123"`  |

### 🔹 To Number
| Method                | Example                | Output   |
|------------------------|------------------------|----------|
| `Number(value)`        | `Number("123")`        | `123`    |
| `parseInt(value)`      | `parseInt("123px")`    | `123`    |
| `parseFloat(value)`    | `parseFloat("123.45")` | `123.45` |
| `+value` (unary plus)  | `+"123"`               | `123`    |

### 🔹 To Boolean
| Method               | Example        | Output  |
|----------------------|----------------|---------|
| `Boolean(value)`     | `Boolean("")`  | `false` |
| `!!value` (double !) | `!!"hello"`    | `true`  |

### Example
```js
String(123);            // "123"
(123).toString();       // "123"

Number("42");           // 42
parseFloat("3.14abc");  // 3.14
+"99";                  // 99

Boolean(0);             // false
!!"hello";              // true
```


# 🟦 14. Common Built-in Methods
| Category  | Method Example                         | Description                                 |
|-----------|----------------------------------------|---------------------------------------------|
| Type Check| `typeof "hello"`                       | Returns the type (e.g., `"string"`)         |
| Array     | `array.push("x")`                      | Add to end of array                         |
|           | `array.pop()`                          | Remove from end                             |
|           | `array.shift()`                        | Remove from start                           |
|           | `array.unshift("x")`                   | Add to start                                |
|           | `array.includes("x")`                  | Check if value exists in array              |
|           | `array.join(", ")`                     | Join array elements into a string           |
|           | `array.reverse()`                      | Reverse the array in place                  |
| String    | `"hi".toUpperCase()`                   | → `"HI"` (convert to uppercase)             |
|           | `"HELLO".toLowerCase()`                | → `"hello"` (convert to lowercase)          |
|           | `"hello".slice(1, 3)`                  | → `"el"` (substring from index 1 to 3)      |
|           | `"a,b,c".split(",")`                   | → `["a", "b", "c"]` (split string to array) |
|           | `"hello".includes("ell")`              | → `true` (check if substring exists)        |
| Math      | `Math.random()`                        | Random number between 0 and 1               |
|           | `Math.floor(4.9)`                      | Round down → `4`                            |
|           | `Math.ceil(4.1)`                       | Round up → `5`                              |
|           | `Math.round(4.6)`                      | Round to nearest → `5`                      |
|           | `Math.max(1, 2, 3)`                    | Find max → `3`                              |
|           | `Math.min(1, 2, 3)`                    | Find min → `1`                              |


