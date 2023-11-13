### Object Methods and Operations in JavaScript

1. **Object Creation:**
   - **Description:** Creating a new object using the object literal notation.
   - **Mutability:** Immutable - The structure of the object can be modified, but the object itself is mutable.

   ```javascript
   const person = {
     name: "John",
     age: 30,
     job: "Developer"
   };
   ```

2. **Object Property Access:**
   - **Description:** Accessing object properties using dot notation.
   - **Mutability:** Immutable - Accessing properties does not modify the object.

   ```javascript
   const person = {
     name: "John",
     age: 30,
     job: "Developer"
   };

   console.log(person.name); // Output: John
   ```

3. **Object Property Assignment:**
   - **Description:** Assigning a new value to an existing object property.
   - **Mutability:** Mutable - Modifies the original object.

   ```javascript
   const person = {
     name: "John",
     age: 30,
     job: "Developer"
   };

   person.age = 31;
   console.log(person); // Output: { name: 'John', age: 31, job: 'Developer' }
   ```

4. **Object Property Deletion:**
   - **Description:** Deleting a property from an object.
   - **Mutability:** Mutable - Modifies the original object.

   ```javascript
   const person = {
     name: "John",
     age: 30,
     job: "Developer"
   };

   delete person.job;
   console.log(person); // Output: { name: 'John', age: 30 }
   ```

5. **Object.keys():**
   - **Description:** Returns an array containing the names of all enumerable properties of an object.
   - **Mutability:** Immutable - Does not modify the original object.

   ```javascript
   const person = {
     name: "John",
     age: 30,
     job: "Developer"
   };

   const keys = Object.keys(person);
   console.log(keys); // Output: ['name', 'age', 'job']
   ```

6. **Object.values():**
   - **Description:** Returns an array containing the values of all enumerable properties of an object.
   - **Mutability:** Immutable - Does not modify the original object.

   ```javascript
   const person = {
     name: "John",
     age: 30,
     job: "Developer"
   };

   const values = Object.values(person);
   console.log(values); // Output: ['John', 30, 'Developer']
   ```

7. **Object.assign():**
   - **Description:** Copies the values of all enumerable properties from one or more source objects to a target object.
   - **Mutability:** Mutable - Modifies the original target object.

   ```javascript
   const person = {
     name: "John",
     age: 30
   };

   const details = {
     job: "Developer",
     location: "City"
   };

   const mergedObject = Object.assign({}, person, details);
   console.log(mergedObject);
   // Output: { name: 'John', age: 30, job: 'Developer', location: 'City' }
   ```

8. **Object.freeze():**
   - **Description:** Freezes an object, preventing new properties from being added and existing properties from being removed or modified.
   - **Mutability:** Immutable - Makes the object itself immutable.

   ```javascript
   const person = {
     name: "John",
     age: 30
   };

   Object.freeze(person);
   person.job = "Developer"; // This won't have any effect.
   console.log(person); // Output: { name: 'John', age: 30 }
   ```
