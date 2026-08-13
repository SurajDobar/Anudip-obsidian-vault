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
- [Conditionals](#"Conditionals")
  - [If Else Statement](#"If""Else""Statement")
  - [Switch Case Statement](#"Switch""Case""Statement")
- [DOM Manipulation](#"DOM""Manipulation")
  - [Click Counter Example](#"Click""Counter""Example")
- [Loops](#"Loops")
  - [For Loop](#"For""Loop")
  - [While Loop](#"While""Loop")
  - [Do While Loop](#"Do""While""Loop")
  - [For Of Loop](#"For""Of""Loop")
- [JavaScript Events](#"JavaScript""Events")
  - [What Are Events](#"What""Are""Events")
- [Mouse Events](#"Mouse""Events")
  - [Onclick Event](#"Onclick""Event")
  - [OnDoubleClick Event](#"OnDoubleClick""Event")
  - [OnMouseDown Event](#"OnMouseDown""Event")
  - [OnMouseOver Event](#"OnMouseOver""Event")
  - [OnMouseUp Event](#"OnMouseUp""Event")
  - [Mouse Events Summary](#"Mouse""Events""Summary")
- [Form Events](#"Form""Events")
  - [OnSubmit Event](#"OnSubmit""Event")
  - [OnFocus Event](#"OnFocus""Event")
  - [OnBlur Event](#"OnBlur""Event")
  - [OnInput Event](#"OnInput""Event")
  - [OnChange Event](#"OnChange""Event")
  - [OnInvalid Event](#"OnInvalid""Event")
  - [Form Events Summary](#"Form""Events""Summary")

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

---

# Day 8

## Conditionals

##### If / Else Statement
The `if/else` statement executes different code blocks based on a condition. If the condition is `true`, the `if` block runs; otherwise, the `else` block runs. You can chain multiple conditions with `else if`. The condition inside `if()` must evaluate to a boolean (`true` or `false`). JavaScript implicitly converts non-boolean values to booleans — truthy values (non-empty strings, non-zero numbers, objects) become `true`, falsy values (`0`, `""`, `null`, `undefined`, `NaN`, `false`) become `false`.

```javascript
let count = 0;
let message;

if (count < 18) {
  message = "Good day";
} else {
  message = "Good evening";
}

console.log(message);  // "Good day"
```

```javascript
// Multiple conditions with else if
let score = 85;
let grade;

if (score >= 90) {
  grade = "A";
} else if (score >= 80) {
  grade = "B";
} else if (score >= 70) {
  grade = "C";
} else {
  grade = "F";
}

console.log(grade);  // "B"
```

**Interview point:** JavaScript uses "truthy" and "falsy" values. Falsy: `0`, `""`, `null`, `undefined`, `NaN`, `false`. Everything else is truthy, including `"0"`, `[]`, `{}`, and `new Boolean(false)`. This is why `if("0")` runs the `if` block — the string `"0"` is truthy.

##### Switch Case Statement
The `switch` statement provides an alternative to multiple `else if` chains. It evaluates an expression and matches it against multiple `case` values. When a match is found, that case's code runs. The `break` statement exits the switch — without it, execution "falls through" to the next case. The `default` case handles unmatched values (like `else`). Switch is cleaner than long `if/else if` chains when comparing one value against many options.

```javascript
let count = 5;

switch (true) {
  case count < 10:
    console.log("Morning");
    break;
  case count < 18:
    console.log("Afternoon");
    break;
  case count < 24:
    console.log("Evening");
    break;
  default:
    console.log("Night");
}
// Output: "Morning"
```

```javascript
// Classic switch with value matching
let day = "Monday";

switch (day) {
  case "Monday":
  case "Tuesday":
  case "Wednesday":
  case "Thursday":
  case "Friday":
    console.log("Weekday");
    break;
  case "Saturday":
  case "Sunday":
    console.log("Weekend");
    break;
  default:
    console.log("Invalid day");
}
// Output: "Weekday"
```

**Interview point:** Switch uses strict comparison (`===`) internally. Don't forget `break` — missing breaks cause fall-through behavior (multiple cases execute). You can group cases by stacking them (no code between cases) for shared logic. Switch `true` allows matching against conditions, not just values.

---

## DOM Manipulation

##### Click Counter Example
A practical example combining variables, DOM manipulation, conditionals, and event handling. The counter increments on each button click, and the page displays different messages based on the count value. Key DOM methods: `document.getElementById()` selects an element by its ID, `.innerHTML` sets the HTML content of that element, and `onclick` attribute attaches a click event handler.

```html
<p id="demo">Good afternoon</p>
<button onclick="clickcount()">Click me</button>
<p id="demo1"></p>
<p id="demo2"></p>

<script>
let count = 0;
let message;

function clickcount() {
  count++;

  // Update counter display
  document.getElementById("demo1").innerHTML = count;

  // if/else conditional
  if (count < 18) {
    message = "Good day";
  } else {
    message = "Good evening";
  }

  document.getElementById("demo").innerHTML = message;

  // switch case conditional
  switch (true) {
    case count < 10:
      document.getElementById("demo2").innerHTML = "Morning";
      break;
    case count < 18:
      document.getElementById("demo2").innerHTML = "Afternoon";
      break;
    case count < 24:
      document.getElementById("demo2").innerHTML = "Evening";
      break;
    default:
      document.getElementById("demo2").innerHTML = "Night";
  }
}
</script>
```

**Interview point:** `innerHTML` replaces all content inside an element (including HTML tags). For plain text, use `.textContent` (faster and safer — prevents XSS attacks). `document.getElementById()` is the most common way to select elements, but modern JavaScript also offers `document.querySelector()` for CSS-selector-based selection.

---

## Loops

##### For Loop
The `for` loop runs a block of code a specific number of times. It has three parts: `initialization` (runs once before the loop starts), `condition` (checked before each iteration — loop stops when `false`), and `iteration` (runs after each iteration, usually incrementing the counter). The `for` loop is the most common loop type — use it when you know exactly how many times to iterate.

```javascript
// Basic for loop: prints 0 to 9
for (let i = 0; i < 10; i++) {
  document.write(i + "<br>");
}
// Output: 0 1 2 3 4 5 6 7 8 9
```

```javascript
// For loop with array
let fruits = ["apple", "banana", "mango"];

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
// Output: apple banana mango
```

```javascript
// Reverse for loop
for (let i = 10; i >= 0; i--) {
  console.log(i);
}
// Output: 10 9 8 7 6 5 4 3 2 1 0
```

**Interview point:** `let` in the for loop creates a new scope for each iteration (block scope). `var` in a for loop creates function scope — all iterations share the same variable, which causes bugs with closures and async code. Always use `let` in for loops.

##### While Loop
The `while` loop runs a block of code **as long as the condition is true**. The condition is checked **before** each iteration. If the condition is `false` from the start, the loop body never executes. Use `while` when you don't know how many times to loop — the loop runs until the condition changes. Always ensure the condition eventually becomes `false` to avoid infinite loops.

```javascript
let i = 0;

while (i < 11) {
  if (i % 2 == 0) {
    document.write(i + "<br>");
  }
  i++;
}
// Output: 0 2 4 6 8 10
```

```javascript
// Practical example: keep asking until valid input
let password = "";
while (password !== "secret") {
  password = prompt("Enter password:");
}
console.log("Access granted!");
```

**Interview point:** The `while` loop checks the condition **before** running the body. If you need the body to run at least once, use `do...while`. Always include a way to exit the loop (incrementing a counter, user input, or breaking condition) to prevent infinite loops that freeze the browser.

##### Do...While Loop
The `do...while` loop is similar to `while`, but the condition is checked **after** the body runs. This guarantees the loop body executes **at least once**, even if the condition is `false` from the start. Use `do...while` when you need to execute code first and validate afterward — like displaying a menu, processing input, or showing a form before checking if data is valid.

```javascript
let i = 0;

do {
  if (i % 2 != 0) {
    document.write(i + "<br>");
  }
  i++;
} while (i < 10);
// Output: 1 3 5 7 9
```

```javascript
// Practical example: display menu at least once
let choice;
do {
  choice = prompt("1. Play\n2. Settings\n3. Exit\nChoose:");
  console.log("You chose:", choice);
} while (choice !== "3");
```

**Interview point:** `while` = condition first (may not run at all), `do...while` = body first (runs at least once). The key difference: `while` can skip entirely, `do...while` always runs once. Use `do...while` for menus, prompts, and input validation where you need to show something before checking.

##### For...Of Loop
The `for...of` loop iterates over **iterable objects** — arrays, strings, Maps, Sets, and any object with a `[Symbol.iterator]` method. It gives you the **values** directly without needing an index. Cleaner and more readable than a traditional `for` loop when you just need the values. Unlike `for...in` (which iterates over object keys/properties), `for...of` iterates over values.

```javascript
let fruits = ["apple", "banana", "mango", "grapes"];

for (let fruit of fruits) {
  document.write(fruit + "<br>");
}
// Output: apple banana mango grapes
```

```javascript
// Iterating over a string
let word = "Hello";

for (let char of word) {
  console.log(char);
}
// Output: H e l l o
```

```javascript
// Iterating over a Map
let scores = new Map([["Alice", 95], ["Bob", 87]]);

for (let [name, score] of scores) {
  console.log(`${name}: ${score}`);
}
// Output: Alice: 95, Bob: 87
```

**Interview point:** `for...of` gives values, `for...in` gives keys/indices. Use `for...of` for arrays and strings (values). Use `for...in` for object properties (keys). The traditional `for` loop gives you both index and value — use it when you need the index position. `for...of` does NOT work on plain objects — use `for...in` or `Object.keys()/Object.values()/Object.entries()` for objects.

---

> **Remember:** `if/else` handles conditional logic. `switch` is cleaner for matching one value against many cases — always use `break`. `for` loop = known iterations, `while` = condition first (may skip), `do...while` = body first (runs once minimum), `for...of` = values of iterables (arrays, strings). Always use `let` in loops, never `var`. `innerHTML` sets content, `getElementById()` selects elements.

---

# Day 9

## JavaScript Events

##### What Are Events
Events are actions or occurrences that happen in the browser — user clicks, key presses, mouse movements, form submissions, page loads, or any interaction. JavaScript can "listen" for these events and execute code in response. This is what makes web pages interactive. You can handle events using HTML attributes (`onclick`), JavaScript properties (`element.onclick`), or the modern `addEventListener()` method. Events are the core of front-end interactivity — every button click, form submission, hover effect, and keyboard shortcut is powered by events.

---

## Mouse Events

##### Onclick Event
The `onclick` event fires when the user clicks an element. It's the most commonly used event. Attach it directly in HTML with the `onclick` attribute, or in JavaScript using `element.onclick` or `addEventListener("click", ...)`. The event handler can call a function or execute inline code.

```html
<button onclick="welcome()">Click me</button>

<script>
function welcome() {
  alert("Onclick event is triggered");
}
</script>
```

##### OnDoubleClick Event
The `ondblclick` event fires when the user double-clicks an element. Two rapid clicks trigger this event. Useful for edit-on-double-click patterns, image zoom, or file open behavior (like desktop file managers).

```html
<h1 id="text">Double click to change color</h1>
<button ondblclick="changecolor()">Double Click</button>

<script>
function changecolor() {
  document.getElementById("text").style.color = "red";
}
</script>
```

##### OnMouseDown Event
The `onmousedown` event fires when the user presses a mouse button down (before releasing it). Fires before `onclick`. Useful for drag-and-drop, drawing applications, or detecting button hold. The opposite is `onmouseup`.

```html
<button onmousedown="alert('Mouse button pressed')">Hold me</button>
```

##### OnMouseOver Event
The `onmouseover` event fires when the mouse cursor enters an element's area. Commonly used for hover effects — showing tooltips, changing styles, or revealing hidden content. The opposite is `onmouseout` (cursor leaves the element).

```html
<button onmouseover="alert('Mouse entered')">Hover me</button>
```

##### OnMouseUp Event
The `onmouseup` event fires when the user releases a mouse button after pressing it. Fires after `onclick`. Used in combination with `onmousedown` for drag-and-drop, custom button press effects, or measuring click duration.

```html
<button onmouseup="alert('Mouse released')">Release me</button>
```

##### Mouse Events Summary

| Event | When It Fires |
|-------|---------------|
| `onclick` | Element is clicked (press + release) |
| `ondblclick` | Element is double-clicked |
| `onmousedown` | Mouse button is pressed down |
| `onmouseup` | Mouse button is released |
| `onmouseover` | Mouse enters the element |
| `onmouseout` | Mouse leaves the element |
| `onmousemove` | Mouse moves inside the element |

**Interview point:** Event order: `onmousedown` → `onmouseup` → `onclick` → `ondblclick`. For hover effects, use `onmouseover`/`onmouseout`. For click actions, use `onclick`. `onmousedown` fires even if the user moves the mouse away before releasing — this is important for drag-and-drop behavior.

---
day 9
## Form Events

##### OnSubmit Event
The `onsubmit` event fires when a form is submitted (user clicks submit button or presses Enter). Use `return false` to prevent the default form submission (which reloads the page). This is essential for client-side form validation — validate the data first, then submit with JavaScript or AJAX if valid.

```html
<form onsubmit="alert('Form submitted'); return false;">
  <input type="text" placeholder="Enter your name">
  <button type="submit">Submit</button>
</form>
```

**Interview point:** `return false` in the event handler prevents the default browser behavior (page reload). In modern code, use `event.preventDefault()` instead — it's cleaner and more explicit.

##### OnFocus Event
The `onfocus` event fires when an element receives focus — user clicks on an input, tabs into it, or focuses it programmatically. Useful for highlighting focused fields, showing help text, or expanding input areas. The opposite is `onblur`.

```html
<input type="text" onfocus="alert('Focus event triggered')" placeholder="Click here">
```

##### OnBlur Event
The `onblur` event fires when an element loses focus — user clicks away, tabs to the next field, or presses Escape. Commonly used for form validation — validate input when the user finishes typing (not on every keystroke). More user-friendly than validating on every input change.

```html
<input type="text" onblur="alert('Blur event triggered')" placeholder="Type then click away">
```

##### OnInput Event
The `oninput` event fires every time the value of an input changes — on every keystroke, paste, or cut. Useful for real-time character counting, live search filtering, or instant preview of user input. Fires continuously as the user types.

```html
<input type="text" oninput="alert('Input event triggered')" placeholder="Start typing...">
```

##### OnChange Event
The `onchange` event fires when the value changes AND the element loses focus (for text inputs) or when a selection is made (for dropdowns, checkboxes, radio buttons). Unlike `oninput`, it doesn't fire on every keystroke — only when the user finishes changing the value. Better for select dropdowns and checkbox toggles.

```html
<input type="text" onchange="alert('Change event triggered')">

<select onchange="alert('Selected: ' + this.value)">
  <option value="html">HTML</option>
  <option value="css">CSS</option>
  <option value="js">JavaScript</option>
</select>
```

##### OnInvalid Event
The `oninvalid` event fires when an input fails HTML5 validation — required field is empty, email format is wrong, number is out of range. This triggers when the user tries to submit the form. Use it to show custom error messages instead of browser defaults.

```html
<form>
  <input type="email" oninvalid="alert('Email is invalid')" required>
  <button type="submit">Submit</button>
</form>
```

##### Form Events Summary

| Event | When It Fires |
|-------|---------------|
| `onsubmit` | Form is submitted |
| `onfocus` | Input receives focus (click/tab into) |
| `onblur` | Input loses focus (click away/tab out) |
| `oninput` | Value changes (every keystroke) |
| `onchange` | Value changes + loses focus |
| `oninvalid` | Input fails validation |

**Interview point:** `oninput` fires on every keystroke (real-time feedback). `onchange` fires when the user finishes editing (blur + change). Use `oninput` for live search/character count. Use `onchange` for select dropdowns and form validation. `onblur` is the most common place to run validation — after the user finishes typing.

---

> **Remember:** Events make pages interactive. `onclick` = click, `ondblclick` = double-click, `onmouseover` = hover in, `onmouseout` = hover out. Form events: `onsubmit` (validate before sending), `onfocus`/`onblur` (input focus), `oninput` (every keystroke), `onchange` (value finalized), `oninvalid` (validation failed). Use `event.preventDefault()` instead of `return false` in modern code.
