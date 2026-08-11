- [JavaScript Basics](#"JavaScript""Basics")
  - [What Is JavaScript](#"What""Is""JavaScript")
  - [Why JavaScript Is Interpreted](#"Why""JavaScript""Is""Interpreted")
  - [Features Of JavaScript](#"Features""Of""JavaScript")
- [Adding JavaScript To HTML](#"Adding""JavaScript""To""HTML")
  - [Script Tag In Head](#"Script""Tag""In""Head")
  - [Script Tag In Body](#"Script""Tag""In""Body")
  - [External JavaScript File](#"External""JavaScript""File")
- [JavaScript Comments](#"JavaScript""Comments")
- [Variables In JavaScript](#"Variables""In""JavaScript")
  - [Var Declaration](#"Var""Declaration")
  - [Let Declaration](#"Let""Declaration")
  - [Const Declaration](#"Const""Declaration")
  - [Auto Variable Declaration](#"Auto""Variable""Declaration")
- [Variable Scope](#"Variable""Scope")
  - [Global Variable](#"Global""Variable")
  - [Local Variable](#"Local""Variable")
- [JavaScript Data Types](#"JavaScript""Data""Types")
  - [Primitive Types](#"Primitive""Types")
  - [Reference Types](#"Reference""Types")
  - [Typeof Operator](#"Typeof""Operator")
- [Operators In JavaScript](#"Operators""In""JavaScript")
  - [Arithmetic Operators](#"Arithmetic""Operators")
  - [Comparison Operators](#"Comparison""Operators")
  - [Logical Operators](#"Logical""Operators")
  - [Assignment Operators](#"Assignment""Operators")

---

# JavaScript Basics

##### What Is JavaScript
JavaScript is a high-level, object-oriented scripting language that makes web pages interactive. While HTML provides structure and CSS provides style, JavaScript provides behavior — it handles user interactions like button clicks, form validation, animations, dynamic content updates, and API calls. JavaScript runs directly in the browser (client-side) without needing a server, making it one of the most versatile and widely-used programming languages in the world. It's not the same as Java — they're completely different languages that just share a similar name.

**Interview point:** HTML = structure, CSS = style, JavaScript = behavior. The three form the foundation of every website. JavaScript was created in 10 days by Brendan Eich in 1995 at Netscape.

##### Why JavaScript Is Interpreted
JavaScript is called an "interpreted" language because it is **not compiled** into machine code before execution. Instead, the browser reads the JavaScript code **line by line** and executes it directly at runtime. This is different from compiled languages like C or Java, where code is converted to machine code first, then executed. The browser's JavaScript engine (V8 in Chrome, SpiderMonkey in Firefox) handles parsing, interpreting, and optimizing the code on the fly. This makes development faster — you write code, save, refresh the browser, and see results immediately.

**Interview point:** JavaScript is technically "just-in-time compiled" (JIT) — modern engines optimize hot code paths into machine code at runtime for better performance. But conceptually, it's still considered interpreted because you don't compile before running.

##### Features Of JavaScript
JavaScript has several key features that make it powerful for web development:

1. **Multi-platform** — Runs in any browser on any operating system (Windows, Mac, Linux, mobile). Write once, run everywhere.
2. **DOM Manipulation** — The Document Object Model lets JavaScript access and modify any HTML element on the page — change text, colors, visibility, add/remove elements, respond to user actions.
3. **Event Handling** — JavaScript listens for user actions (clicks, key presses, mouse movements, form submissions) and responds with custom logic. This is what makes web pages interactive.
4. **OOP Support** — Supports object-oriented programming with classes, objects, inheritance, and encapsulation. Also supports functional programming.
5. **Built-in Methods** — Provides hundreds of built-in methods for strings, arrays, dates, math, JSON, and more. You rarely need to write utilities from scratch.
6. **Asynchronous** — Supports async operations like API calls, timers, and promises without blocking the main thread. This keeps pages responsive while loading data.
7. **Event-driven** — Code executes in response to events (user clicks, page loads, data arrives), not in a linear sequence.

---

## Adding JavaScript To HTML

##### Script Tag In Head
Place JavaScript inside `<script>` tags in the `<head>` section. The code runs before the page body loads. The `type="text/javascript"` attribute specifies the MIME type (optional in HTML5 — browsers default to JavaScript). Functions defined here are available to all elements in the body. However, placing scripts in `<head>` can slow down page load because the browser must download and execute the script before rendering the page body.

```html
<head>
  <script type="text/javascript">
    function myFunction() {
      alert("Hello World!!");
    }
  </script>
</head>
<body>
  <input type="button" value="Click me" onclick="myFunction()" />
</body>
```

##### Script Tag In Body
Place JavaScript at the bottom of the `<body>` section, after all HTML content. This is better for page performance — the browser renders the visible content first, then loads the script. The user sees the page faster. This is the recommended placement for inline scripts in modern web development. Scripts at the bottom can access all HTML elements above them because those elements have already been parsed.

```html
<body>
  <h1>Page loads first</h1>
  <p>Content is visible immediately</p>

  <script type="text/javascript">
    alert("This runs after the page loads");
  </script>
</body>
```

##### External JavaScript File
Link an external `.js` file using the `<script>` tag with the `src` attribute. This is the **best and most common method** for real projects. Benefits: separate files keep HTML clean, one JS file can be shared across multiple HTML pages, browser caching improves performance (file loads once, then from cache), and multiple developers can work on HTML and JS separately. The `src` attribute points to the file path. Don't mix inline scripts with `src` on the same `<script>` tag — the inline code will be ignored.

```html
<!-- external JS file linked in head -->
<head>
  <script src="script.js" type="text/javascript"></script>
</head>
<body>
  <input type="button" value="Click me" onclick="myFunction()" />
</body>
```

**script.js**
```javascript
function myFunction() {
  alert("External JavaScript File");
}
```

**Interview point:** Always place `<script>` tags at the bottom of `<body>` or use the `defer` attribute (`<script src="app.js" defer></script>`) to prevent blocking page rendering. The `defer` attribute downloads the script in parallel with HTML parsing and executes it after parsing is complete.

---

## JavaScript Comments

##### Single Line Comments
Use `//` to comment a single line. The browser ignores everything after `//` on that line. Comments are essential for explaining complex logic, marking TODO items, and debugging (temporarily disabling code).

```javascript
// This is a single line comment
let x = 10; // This comment explains what x is
```

##### Multi Line Comments
Use `/* */` to comment multiple lines. Everything between `/*` and `*/` is ignored by the browser. Useful for longer explanations, function documentation, and temporarily disabling blocks of code.

```javascript
/* This is a multi-line comment.
   It can span multiple lines.
   Useful for longer explanations. */

/*
  function disabled() {
    console.log("This code won't run");
  }
*/
```

**Interview point:** Comments are ignored by the JavaScript engine — they have zero performance impact. Good code is self-documenting, but comments explain **why** you did something, not **what** the code does. Use JSDoc-style comments (`/** */`) for function documentation that tools can parse.

---

## Variables In JavaScript

Variables are containers for storing data values. JavaScript has four ways to declare variables, each with different behavior regarding scope, reassignment, and hoisting.

##### Var Declaration
`var` is the original way to declare variables in JavaScript (pre-ES6). It has **function scope** — accessible anywhere within the function it's declared in, regardless of block boundaries. `var` variables are **hoisted** (moved to the top of their scope during compilation) and initialized as `undefined`. `var` allows **redeclaration** and **reassignment**. In modern JavaScript, `var` is rarely used — `let` and `const` are preferred because they have more predictable block scoping behavior.

```javascript
var a = 10;
console.log(a);  // 10

var a = 20;      // redeclaration allowed (potential bug)
console.log(a);  // 20

a = 30;          // reassignment allowed
console.log(a);  // 30
```

##### Let Declaration
`let` is the modern way to declare variables that can be reassigned. It has **block scope** — only accessible within the nearest set of curly braces `{ }` where it's declared. `let` variables are **not redeclarable** in the same scope (prevents accidental overwriting). They are hoisted but not initialized — accessing them before declaration causes a `ReferenceError` (temporal dead zone). Use `let` when the variable's value will change (counters, loop variables, temporary values).

```javascript
let b = 20;
console.log(b);  // 20

b = 25;          // reassignment allowed
console.log(b);  // 25

// let b = 30;   // ERROR: cannot redeclare in same scope

{
  let inside = 100;
  console.log(inside);  // 100
}
// console.log(inside); // ERROR: outside block scope
```

##### Const Declaration
`const` declares variables that **cannot be reassigned** after initialization. They have **block scope** like `let`. `const` prevents reassignment of the variable binding, but for objects and arrays, the contents CAN still be modified (the reference is constant, not the data). Use `const` for values that should never change (configuration values, API URLs, mathematical constants, DOM element references). Always prefer `const` over `let` unless you know the value will change.

```javascript
const c = 30;
console.log(c);  // 30

// c = 40;       // ERROR: Assignment to constant variable

const person = { name: "John" };
person.name = "Jane";  // OK: object contents can change
console.log(person);   // { name: "Jane" }

// person = {};        // ERROR: cannot reassign the reference
```

##### Auto Variable Declaration
Declaring a variable without `var`, `let`, or `const` creates an **implicit global variable**. This is **bad practice** — the variable becomes accessible from anywhere in the code, even outside functions, leading to naming conflicts, bugs, and hard-to-debug code. Always use `var`, `let`, or `const`. In strict mode (`"use strict"`), auto-declaration throws an error, which is the correct behavior.

```javascript
d = 40;          // implicit global variable (BAD PRACTICE)
console.log(d);  // 40

// In strict mode, this throws a ReferenceError
```

**Interview point:** Always use `const` by default, `let` when reassignment is needed, and never use `var` in modern code. Never create implicit globals. The rules: `const` = constant reference, `let` = block-scoped reassignable, `var` = function-scoped (legacy).

---

## Variable Scope

##### Global Variable
A global variable is declared **outside** any function or block. It's accessible from anywhere in the code — inside functions, inside blocks, from external scripts. Global variables persist for the entire lifetime of the page. Use sparingly — too many globals pollute the global namespace, increase naming collision risk, and make code harder to maintain and test.

```javascript
var a = 10;  // global variable

function myFunction() {
  console.log(a);  // accessible inside function
}

myFunction();  // 10
console.log(a); // 10 (accessible outside too)
```

##### Local Variable
A local variable is declared **inside** a function or block. It's only accessible within that function/block. Local variables are created when the function is called and destroyed when the function returns. Different functions can have local variables with the same name without conflict — they're completely separate.

```javascript
function myFunction() {
  var b = 20;  // local variable
  console.log(b);  // 20
}

myFunction();
// console.log(b);  // ERROR: b is not defined outside function
```

**Interview point:** Scope determines where variables are accessible. `var` = function scope, `let`/`const` = block scope. Block scope is stricter and more predictable — a variable declared inside an `if` block or `for` loop is only accessible inside that block. This prevents bugs where variables "leak" out of loops or conditionals.

---

## JavaScript Data Types

JavaScript has two categories of data types: **primitive** (stored by value) and **reference** (stored by reference).

##### Primitive Types
Primitive types hold a single value and are compared by value. There are 7 primitive types:

| Type | Description | Example |
|------|-------------|---------|
| `Number` | Integers and decimals | `10`, `3.14`, `-5` |
| `String` | Text data (in quotes) | `"Hello"`, `'World'`, `` `Template` `` |
| `Boolean` | True or false | `true`, `false` |
| `undefined` | Variable declared but no value assigned | `let x;` |
| `null` | Intentional absence of value | `let y = null;` |
| `Symbol` | Unique identifier (ES6+) | `Symbol("id")` |
| `BigInt` | Very large integers (ES2020+) | `123n`, `BigInt(123)` |

```javascript
let num = 10;
let str = "Hello";
let bool = true;
let undef;                    // undefined
let empty = null;             // null
let sym = Symbol("hello");
let big = 123n;
```

##### Reference Types
Reference types store a reference (memory address) to the actual data, not the data itself. Two variables can reference the same object — changing one affects the other. Reference types include objects, arrays, and functions.

| Type | Description | Example |
|------|-------------|---------|
| `Object` | Key-value pairs | `{ name: "John", age: 25 }` |
| `Array` | Ordered list | `[1, 2, 3, 4, 5]` |
| `Function` | Reusable code block | `function greet() {}` |

```javascript
let obj = { name: "John" };
let arr = [1, 2, 3];
function greet() { return "Hello"; }

console.log(typeof obj);  // "object"
console.log(typeof arr);  // "object" (arrays are objects in JS)
console.log(typeof greet); // "function"
```

**Interview point:** Arrays return `"object"` with `typeof` — use `Array.isArray(arr)` to properly check if something is an array. `null` also returns `"object"` with `typeof` — this is a known JavaScript bug that has existed since the language was created.

##### Typeof Operator
The `typeof` operator returns a string indicating the type of the operand. It's the primary way to check data types in JavaScript. Returns: `"number"`, `"string"`, `"boolean"`, `"undefined"`, `"object"`, `"function"`, `"symbol"`, `"bigint"`.

```javascript
typeof 123          // "number"
typeof "Hello"      // "string"
typeof true         // "boolean"
typeof undefined    // "undefined"
typeof null         // "object" (historical bug)
typeof {}           // "object"
typeof []           // "object"
typeof function(){} // "function"
typeof Symbol("hi") // "symbol"
typeof 123n         // "bigint"
```

**Interview point:** `typeof` has two well-known quirks: `typeof null` returns `"object"` (a bug from JavaScript's first implementation that was never fixed for backward compatibility), and `typeof []` returns `"object"` (arrays are objects). Always use `Array.isArray()` to check for arrays.

---

## Operators In JavaScript

##### Arithmetic Operators
Used for mathematical calculations:

| Operator | Name | Example | Result |
|----------|------|---------|--------|
| `+` | Addition | `10 + 5` | `15` |
| `-` | Subtraction | `10 - 5` | `5` |
| `*` | Multiplication | `10 * 5` | `50` |
| `/` | Division | `10 / 5` | `2` |
| `%` | Modulus (remainder) | `10 % 3` | `1` |
| `**` | Exponentiation | `2 ** 3` | `8` |
| `++` | Increment | `x++` | `x + 1` |
| `--` | Decrement | `x--` | `x - 1` |

```javascript
let a = 10 + 5;    // 15
let b = 10 - 5;    // 5
let c = 10 * 5;    // 50
let d = 10 / 3;    // 3.333...
let e = 10 % 3;    // 1 (remainder)
let f = 2 ** 3;    // 8 (2 cubed)
```

##### Comparison Operators
Used to compare two values. Return `true` or `false`:

| Operator | Name | Description |
|----------|------|-------------|
| `==` | Equal (loose) | Compares values, type coercion happens |
| `===` | Equal (strict) | Compares values AND types |
| `!=` | Not equal (loose) | Values are different |
| `!==` | Not equal (strict) | Values or types are different |
| `>` | Greater than | Left is larger |
| `<` | Less than | Left is smaller |
| `>=` | Greater or equal | Left is larger or equal |
| `<=` | Less or equal | Left is smaller or equal |

```javascript
5 == "5"    // true  (loose: type coercion converts string to number)
5 === "5"   // false (strict: number !== string)
5 != "5"    // false (loose: values are equal after coercion)
5 !== "5"   // true  (strict: different types)
10 > 5      // true
10 < 5      // false
10 >= 10    // true
```

**Interview point:** Always use `===` and `!==` (strict comparison) instead of `==` and `!=` (loose comparison). Loose comparison causes unexpected behavior due to type coercion (`"0" == false` is `true`, `[] == false` is `true`). Strict comparison is predictable and prevents bugs.

##### Logical Operators
Used to combine conditional expressions:

| Operator | Name | Description |
|----------|------|-------------|
| `&&` | AND | Both conditions must be true |
| `\|\|` | OR | At least one condition must be true |
| `!` | NOT | Reverses the boolean value |

```javascript
true && true    // true
true && false   // false
true || false   // true
false || false  // false
!true           // false
!false          // true

// Practical example
let age = 25;
let hasID = true;
if (age >= 18 && hasID) {
  console.log("Entry allowed");
}
```

##### Assignment Operators
Used to assign and update values:

| Operator | Example | Equivalent |
|----------|---------|------------|
| `=` | `x = 10` | `x = 10` |
| `+=` | `x += 5` | `x = x + 5` |
| `-=` | `x -= 5` | `x = x - 5` |
| `*=` | `x *= 5` | `x = x * 5` |
| `/=` | `x /= 5` | `x = x / 5` |
| `%=` | `x %= 5` | `x = x % 5` |

```javascript
let x = 10;
x += 5;   // x = 15
x -= 3;   // x = 12
x *= 2;   // x = 24
x /= 4;   // x = 6
x %= 4;   // x = 2
```

---

> **Remember:** Always use `const` by default, `let` when reassignment is needed. Never use `var` in modern code. Always use `===` for comparison. JavaScript is interpreted (runs line by line in the browser), not compiled. HTML = structure, CSS = style, JavaScript = behavior. Place `<script>` at the bottom of `<body>` or use `defer` for better performance.
