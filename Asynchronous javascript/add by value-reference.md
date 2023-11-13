### Pass by Value and Pass by Reference in JavaScript

In JavaScript, whether a variable is passed by value or by reference depends on the data type.

#### Pass by Value:

When a primitive data type is passed to a function, the function receives a copy of the value, and modifications inside the function do not affect the original variable.

**Example:**

```javascript
function modifyValue(value) {
  value = 10;
}

let number = 5;
modifyValue(number);
console.log(number); // Output: 5
```

In this example, the function `modifyValue` receives a copy of the value of `number`, and changing the value inside the function doesn't affect the original variable.

#### Pass by Reference:

When an object (which includes arrays and functions) is passed to a function, the function receives a reference to the object, not a copy. Modifications inside the function can affect the original object.

**Example:**

```javascript
function modifyArray(arr) {
  arr.push(4);
}

let myArray = [1, 2, 3];
modifyArray(myArray);
console.log(myArray); // Output: [1, 2, 3, 4]
```

In this example, the function `modifyArray` receives a reference to the `myArray` object. The modification (adding an element) inside the function affects the original array.

**Note:** While objects are passed by reference, it's more accurate to say that the reference is passed by value. The reference itself is copied, but both the original and the copy refer to the same object in memory.
