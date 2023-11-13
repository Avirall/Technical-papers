Higher-order functions are functions that can take other functions as arguments or return functions as their results. This concept is a fundamental aspect of functional programming and allows for more expressive and concise code. In JavaScript, functions are first-class citizens, meaning they can be treated like any other variable, and higher-order functions take advantage of this feature.

### Examples of Higher-Order Functions:

#### 1. **`map()`:**

The `map` function applies a provided function to each element in an array and returns a new array containing the results.

```javascript
const numbers = [1, 2, 3, 4, 5];
const squaredNumbers = numbers.map(function (num) {
  return num ** 2;
});
console.log(squaredNumbers); // Output: [1, 4, 9, 16, 25]
```

#### 2. **`filter()`:**

The `filter` function creates a new array with elements that satisfy a provided condition.

```javascript
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(function (num) {
  return num % 2 === 0;
});
console.log(evenNumbers); // Output: [2, 4]
```

#### 3. **`reduce()`:**

The `reduce` function applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```javascript
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce(function (accumulator, num) {
  return accumulator + num;
}, 0);
console.log(sum); // Output: 15
```

#### 4. **`forEach()`:**

The `forEach` function executes a provided function once for each array element.

```javascript
const colors = ['red', 'green', 'blue'];
colors.forEach(function (color) {
  console.log(color);
});
// Output:
// red
// green
// blue
```

#### 5. **`sort()` with a Comparator Function:**

The `sort` function sorts the elements of an array based on a provided comparator function.

```javascript
const fruits = ['banana', 'apple', 'orange'];
const sortedFruits = fruits.sort(function (a, b) {
  return a.localeCompare(b);
});
console.log(sortedFruits); // Output: ['apple', 'banana', 'orange']
```

#### 6. **Function as an Argument:**

Higher-order functions can also take other functions as arguments.

```javascript
function operateOnNumbers(a, b, operation) {
  return operation(a, b);
}

function add(a, b) {
  return a + b;
}

function multiply(a, b) {
  return a * b;
}

console.log(operateOnNumbers(3, 4, add));       // Output: 7
console.log(operateOnNumbers(3, 4, multiply));  // Output: 12
```

#### 7. **Function as a Return Value:**

Higher-order functions can also return functions.

```javascript
function multiplyBy(factor) {
  return function (number) {
    return number * factor;
  };
}

const double = multiplyBy(2);
console.log(double(5)); // Output: 10
```

In this example, `multiplyBy` is a higher-order function that returns a function (`double`) based on the provided factor.
