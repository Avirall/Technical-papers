Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use variables and functions before they are declared in the code. However, it's important to note that only the declarations are hoisted, not the initializations or assignments.

### Variable Hoisting:

```javascript
console.log(x); // Output: undefined
var x = 5;
console.log(x); // Output: 5
```

In this example, the variable `x` is hoisted to the top of the scope during compilation. The first `console.log(x)` outputs `undefined` because the declaration is hoisted, but the assignment is not. The second `console.log(x)` outputs `5` after the variable is assigned.

### Function Hoisting:

```javascript
sayHello(); // Output: Hello!
function sayHello() {
  console.log("Hello!");
}
```

Functions are also hoisted to the top of their scope. In this example, the function `sayHello` is hoisted, and it can be called before the actual declaration in the code.

### Hoisting with `let` and `const`:

```javascript
console.log(y); // ReferenceError: Cannot access 'y' before initialization
let y = 10;
console.log(y); // Output: 10
```

Unlike `var`, variables declared with `let` and `const` are hoisted but not initialized. Accessing them before the declaration results in a `ReferenceError`.

### Function Expressions:

```javascript
sayHi(); // TypeError: sayHi is not a function
var sayHi = function() {
  console.log("Hi!");
};
```

Function expressions are not hoisted in the same way as function declarations. The variable `sayHi` is hoisted, but it's initialized with `undefined`, leading to a `TypeError` when trying to call it before the assignment.
