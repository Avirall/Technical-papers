### String Methods in JavaScript

1. **`String.length` (Length Property):**
   - **Description:** Returns the length of a string.
   - **Mutability:** Immutable - It does not modify the original string.

   ```javascript
   const myString = "Hello, World!";
   const length = myString.length;
   console.log(length); // Output: 13
   ```

2. **`String.concat()` (Concatenation):**
   - **Description:** Combines two or more strings and returns a new string.
   - **Mutability:** Immutable - It does not modify the original strings.

   ```javascript
   const str1 = "Hello";
   const str2 = "World";
   const result = str1.concat(", ", str2, "!");
   console.log(result); // Output: Hello, World!
   ```

3. **`String.indexOf()` (Find Index of Substring):**
   - **Description:** Returns the index of the first occurrence of a specified substring.
   - **Mutability:** Immutable - It does not modify the original string.

   ```javascript
   const myString = "Hello, World!";
   const index = myString.indexOf("World");
   console.log(index); // Output: 7
   ```

4. **`String.slice()` (Substring Extraction):**
   - **Description:** Extracts a section of a string and returns it as a new string.
   - **Mutability:** Immutable - It does not modify the original string.

   ```javascript
   const myString = "Hello, World!";
   const newString = myString.slice(7, 12);
   console.log(newString); // Output: World
   ```

5. **`String.replace()` (Substring Replacement):**
   - **Description:** Replaces a specified substring with another substring.
   - **Mutability:** Immutable - It returns a new string with the replacements, leaving the original string unchanged.

   ```javascript
   const myString = "Hello, World!";
   const newString = myString.replace("World", "Universe");
   console.log(newString); // Output: Hello, Universe!
   ```

6. **`String.toUpperCase()` / `String.toLowerCase()` (Case Conversion):**
   - **Description:** Converts the string to uppercase or lowercase.
   - **Mutability:** Immutable - They do not modify the original string.

   ```javascript
   const myString = "Hello, World!";
   const upperCase = myString.toUpperCase();
   const lowerCase = myString.toLowerCase();
   console.log(upperCase); // Output: HELLO, WORLD!
   console.log(lowerCase); // Output: hello, world!
   ```

7. **`String.trim()` (Trim Whitespace):**
   - **Description:** Removes whitespace from both ends of a string.
   - **Mutability:** Immutable - It does not modify the original string.

   ```javascript
   const myString = "   Hello, World!   ";
   const trimmedString = myString.trim();
   console.log(trimmedString); // Output: Hello, World!
   ```
