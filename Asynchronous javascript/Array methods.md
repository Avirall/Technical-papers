### Array Methods in JavaScript

#### Basics:

1. **`Array.pop()` (Remove Last Element):**
   - **Description:** Removes the last element from an array and returns that element.
   - **Mutability:** Mutable - It modifies the original array.

   ```javascript
   const myArray = [1, 2, 3];
   const removedElement = myArray.pop();
   console.log(myArray); // Output: [1, 2]
   console.log(removedElement); // Output: 3
   ```

2. **`Array.push()` (Add Elements to the End):**
   - **Description:** Adds one or more elements to the end of an array.
   - **Mutability:** Mutable - It modifies the original array.

   ```javascript
   const myArray = [1, 2, 3];
   myArray.push(4, 5);
   console.log(myArray); // Output: [1, 2, 3, 4, 5]
   ```

3. **`Array.concat()` (Concatenate Arrays):**
   - **Description:** Concatenates two or more arrays and returns a new array.
   - **Mutability:** Immutable - It does not modify the original arrays.

   ```javascript
   const array1 = [1, 2, 3];
   const array2 = [4, 5];
   const newArray = array1.concat(array2);
   console.log(newArray); // Output: [1, 2, 3, 4, 5]
   console.log(array1); // Output: [1, 2, 3]
   ```

4. **`Array.slice()` (Array Copy/Extraction):**
   - **Description:** Returns a shallow copy of a portion of an array.
   - **Mutability:** Immutable - It does not modify the original array.

   ```javascript
   const myArray = [1, 2, 3, 4, 5];
   const newArray = myArray.slice(1, 4);
   console.log(newArray); // Output: [2, 3, 4]
   console.log(myArray); // Output: [1, 2, 3, 4, 5]
   ```

5. **`Array.splice()` (Add/Remove Elements at a Specific Index):**
   - **Description:** Adds or removes elements from a specific index in an array.
   - **Mutability:** Mutable - It modifies the original array.

   ```javascript
   const myArray = [1, 2, 3, 4, 5];
   const removedElements = myArray.splice(2, 2, 6, 7);
   console.log(myArray); // Output: [1, 2, 6, 7, 5]
   console.log(removedElements); // Output: [3, 4]
   ```

6. **`Array.join()` (Array to String):**
   - **Description:** Joins all elements of an array into a string.
   - **Mutability:** Immutable - It does not modify the original array.

   ```javascript
   const myArray = ['Hello', 'World'];
   const resultString = myArray.join(' ');
   console.log(resultString); // Output: 'Hello World'
   console.log(myArray); // Output: ['Hello', 'World']
   ```

7. **`Array.flat()` (Flatten Nested Arrays):**
   - **Description:** Creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.
   - **Mutability:** Immutable - It does not modify the original array.

   ```javascript
   const nestedArray = [1, [2, [3, 4]]];
   const flattenedArray = nestedArray.flat(2);
   console.log(flattenedArray); // Output: [1, 2, 3, 4]
   console.log(nestedArray); // Output: [1, [2, [3, 4]]]
   ```

#### Finding:

1. **`Array.find()` (Find Element):**
   - **Description:** Returns the first element in the array that satisfies the provided testing function.
   - **Example:**

     ```javascript
     const numbers = [1, 2, 3, 4, 5];
     const result = numbers.find(num => num > 2);
     console.log(result); // Output: 3
     ```

2. **`Array.indexOf()` (Find Index):**
   - **Description:** Returns the first index at which a given element can be found in the array, or -1 if it is not present.
   - **Example:**

     ```javascript
     const fruits = ['apple', 'banana', 'orange'];
     const index = fruits.indexOf('banana');
     console.log(index); // Output: 1
     ```

3. **`Array.includes()` (Check Inclusion):**
   - **Description:** Determines whether an array includes a certain element.
   - **Example:**

     ```javascript
     const colors = ['red', 'green', 'blue'];
     const includesRed = colors.includes('red');
     console.log(includesRed); // Output: true
     ```

4. **`Array.findIndex()` (Find Index with Condition):**
   - **Description:** Returns the index of the first element in the array that satisfies the provided testing function; otherwise, it returns -1.
   - **Example:**

     ```javascript
     const numbers = [1, 2, 3, 4, 5];
     const index = numbers.findIndex(num => num > 2);
     console.log(index); // Output: 2
     ```

#### Higher Order Functions:

1. **`Array.forEach()` (Iterate Over Elements):**
   - **Description:** Executes a provided function once for each array element.
   - **Example:**

     ```javascript
     const numbers = [1, 2, 3];
     numbers.forEach(num => console.log(num));
     // Output:
     // 1
     // 2
     // 3
     ```

2. **`Array.filter()` (Filter Elements):**
   - **Description:** Creates a new array with elements that pass the provided function's test.
   - **Example:**

     ```javascript
     const numbers = [1, 2, 3, 4, 5];
     const evenNumbers = numbers.filter(num => num % 2 === 0);
     console.log(evenNumbers); // Output: [2, 4]
     ```

3. **`Array.map()` (Transform Elements):**
   - **Description:** Creates a new array with the results of calling a provided function on every element in the array.
   - **Example:**

     ```javascript
     const numbers = [1, 2, 3];
     const squaredNumbers = numbers.map(num => num ** 2);
     console.log(squaredNumbers); // Output: [1, 4, 9]
     ```

4. **`Array.reduce()` (Reduce to Single Value):**
   - **Description:** Applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.
   - **Example:**

     ```javascript
     const numbers = [1, 2, 3, 4, 5];
     const sum = numbers.reduce((acc, num) => acc + num, 0);
     console.log(sum); // Output: 15
     ```

5. **`Array.sort()` (Sort Elements):**
   - **Description:** Sorts the elements of an array in place.
   - **Example:**

     ```javascript
     const fruits = ['banana', 'apple', 'orange'];
     fruits.sort();
     console.log(fruits); // Output: ['apple', 'banana', 'orange']
     ```

#### Advanced:

1. **Array Methods Chaining:**
    - **Description:** You can chain multiple array methods together to perform complex operations in a concise manner.
    - **Example:**

      ```javascript
      const numbers = [1, 2, 3, 4, 5];
      const result = numbers
        .filter(num => num % 2 === 0)
        .map(num => num ** 2)
        .reduce((acc, num) => acc + num, 0);
      console.log(result); // Output: 20
      ```
