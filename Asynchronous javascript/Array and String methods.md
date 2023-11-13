### Strings:

#### Mutable Methods:
1. **`strObj.concat()` (Concatenation):**
   - **Description:** Concatenates one or more strings to the end of the calling string.
   - **Mutability:** Immutable - It returns a new string without modifying the original.

#### Immutable Methods:
1. **`strObj.slice()` (Substring Extraction):**
   - **Description:** Extracts a section of a string and returns it as a new string.
   - **Mutability:** Immutable - It does not modify the original string.

2. **`strObj.substring()` (Substring Extraction):**
   - **Description:** Similar to `slice()`, but it has slightly different behavior.
   - **Mutability:** Immutable - It does not modify the original string.

3. **`strObj.replace()` (Substring Replacement):**
   - **Description:** Replaces a specified substring with another substring.
   - **Mutability:** Immutable - It returns a new string with the replacements, leaving the original string unchanged.

4. **`strObj.toUpperCase()` / `strObj.toLowerCase()` (Case Conversion):**
   - **Description:** Converts the string to uppercase or lowercase.
   - **Mutability:** Immutable - They do not modify the original string.

### Arrays:

#### Mutable Methods:
1. **`arr.push()` (Adding Elements):**
   - **Description:** Adds one or more elements to the end of an array.
   - **Mutability:** Mutable - It modifies the original array.

2. **`arr.pop()` (Removing Elements):**
   - **Description:** Removes the last element from an array.
   - **Mutability:** Mutable - It modifies the original array.

3. **`arr.shift()` / `arr.unshift()` (Adding/Removing Elements):**
   - **Description:** Adds or removes elements from the beginning of an array.
   - **Mutability:** Mutable - They modify the original array.

4. **`arr.splice()` (Adding/Removing Elements):**
   - **Description:** Adds or removes elements from a specific index in an array.
   - **Mutability:** Mutable - It modifies the original array.

#### Immutable Methods:
1. **`arr.concat()` (Concatenation):**
   - **Description:** Concatenates two or more arrays and returns a new array.
   - **Mutability:** Immutable - It does not modify the original arrays.

2. **`arr.slice()` (Array Copy/Extraction):**
   - **Description:** Returns a shallow copy of a portion of an array.
   - **Mutability:** Immutable - It does not modify the original array.

3. **`arr.map()` (Element Transformation):**
   - **Description:** Creates a new array by applying a function to each element of the original array.
   - **Mutability:** Immutable - It does not modify the original array.

4. **`arr.filter()` (Element Filtering):**
   - **Description:** Creates a new array with elements that pass a test specified by a function.
   - **Mutability:** Immutable - It does not modify the original array.
