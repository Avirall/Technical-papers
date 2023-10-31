# Python String Methods

Strings are essential in Python for text processing. Python provides a range of string methods to manipulate and work with strings effectively.

## Basic String Operations

1. `len()`: Returns the length of a string.

```
text = "Hello, World!"
length = len(text)  # Result: 13
```

2. `strip()`: Removes leading and trailing white spaces from a string.

```
text = "  Hello, World!  "
cleaned_text = text.strip()  # Result: "Hello, World!"
```

3. `split()`: Splits a string into a list of substrings based on a delimiter.

```
text = "apple,banana,kiwi"
fruits = text.split(",")  # Result: ['apple', 'banana', 'kiwi']
```

4.`join()`: Joins elements of an iterable into a single string using the specified separator.

```
fruits = ['apple', 'banana', 'kiwi']
text = ", ".join(fruits)  # Result: "apple, banana, kiwi"
```

## Searching and Replacing

5. `find()`: Finds the first occurrence of a substring within a string and returns its index. If not found, returns -1.

```
text = "Hello, World!"
index = text.find("World")  # Result: 7
```

6. `replace()`: Replaces all occurrences of a specified substring with another string.

```
text = "Hello, World!"
new_text = text.replace("Hello", "Hi")  # Result: "Hi, World!"
```

7. `count()`: Counts the number of non-overlapping occurrences of a substring in a string.

```
text = "Peter Piper picked a peck of pickled peppers."
count = text.count("peck")  # Result: 2
```

## Case Conversion

8. `lower()`: Converts all characters in a string to lowercase.

```
text = "Hello, World!"
lowercase_text = text.lower()  # Result: "hello, world!"
```

9.`upper()`: Converts all characters in a string to uppercase.

```
text = "Hello, World!"
uppercase_text = text.upper()  # Result: "HELLO, WORLD!"
```

10. `capitalize()`: Capitalizes the first character of a string.

```
text = "hello, world!"
capitalized_text = text.capitalize()  # Result: "Hello, world!"
```
