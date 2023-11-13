## Loops in JS:

### 1. for Loop:
```javascript
for (initialization; condition; iteration) {
  // code to be executed
}
```
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
### Description: 
The for loop is a traditional loop that consists of three parts - initialization, condition, and iteration. It repeatedly executes a block of code as long as the specified condition is true.

### 2. forEach Loop:
```javascript
array.forEach(function(currentValue, index, array) {
  // code to be executed
});
```
```javascript
const numbers = [1, 2, 3, 4, 5];
numbers.forEach(function(number) {
  console.log(number);
});
```
### Description: 
The forEach loop is used specifically with arrays. It calls a provided function once for each element in the array, in order.

### 3. for ... in Loop:
```javascript
for (variable in object) {
  // code to be executed
}
```
```javascript
const person = { name: 'John', age: 30, job: 'Developer' };
for (let key in person) {
  console.log(`${key}: ${person[key]}`);
}
```
### Description: 
The for ... in loop iterates over the enumerable properties of an object, in arbitrary order.

### 4. for ... of Loop:
```javascript
for (variable of iterable) {
  // code to be executed
}
```
```javascript
const fruits = ['apple', 'banana', 'orange'];
for (let fruit of fruits) {
  console.log(fruit);
}
```
### Description: 
The for ... of loop is used to iterate over iterable objects (arrays, strings, etc.) in the order of the values.

###  5. while Loop:
```javascript
while (condition) {
  // code to be executed
}
```
```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```
### Description: 
The while loop repeats a block of code as long as the specified condition is true.
