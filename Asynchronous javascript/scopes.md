In JavaScript, scopes define the regions or contexts in which variables and functions are accessible. Understanding scopes is crucial for writing maintainable and bug-free code. There are two main types of scopes in JavaScript: global scope and local scope.

### Global Scope:

Variables and functions declared outside any function or block have global scope. They are accessible throughout the entire program.

**Example:**

```javascript
// Global variable
var globalVar = "I am global";

function myFunction() {
  // Accessing the global variable
  console.log(globalVar);
}

myFunction(); // Output: I am global
```

In this example, `globalVar` is accessible inside the `myFunction` function because it is declared in the global scope.

### Local Scope:

Variables declared inside a function or block have local scope. They are only accessible within that specific function or block.

**Example:**

```javascript
function myFunction() {
  // Local variable
  var localVar = "I am local";
  console.log(localVar);
}

myFunction(); // Output: I am local
// Accessing localVar outside the function will result in an error
```

Here, `localVar` is declared inside the `myFunction` function and is accessible only within that function.

### Block Scope (ES6 and later):

With the introduction of ES6 (ECMAScript 2015), the `let` and `const` keywords allow the declaration of variables with block scope.

**Example:**

```javascript
if (true) {
  // Block-scoped variable
  let blockVar = "I am block-scoped";
  console.log(blockVar);
}

// Accessing blockVar outside the block will result in an error
```

In this example, `blockVar` is accessible only within the `if` block where it is declared.

### Lexical Scope:

Lexical scope, also known as static scope, refers to how variable access is determined by the placement of variables and functions in the code. Inner functions have access to variables in their outer (enclosing) scope.

**Example:**

```javascript
function outer() {
  var outerVar = "I am outer";

  function inner() {
    // Accessing outerVar from the outer scope
    console.log(outerVar);
  }

  inner();
}

outer(); // Output: I am outer
```

Here, `inner` has access to the `outerVar` variable in the outer scope due to lexical scoping.
