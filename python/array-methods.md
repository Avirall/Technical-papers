# Python List/Array Methods

Python provides a variety of methods for manipulating lists (arrays), making it a versatile language for data manipulation and processing.

## Basic List Operations

1. **`append(x)`**: Adds an item to the end of the list.

   ```
   my_list = [1, 2, 3]
   my_list.append(4)  # Result: [1, 2, 3, 4]
   ```

2. **`extend(iterable)`**: Extends the list by appending elements from an iterable.

```
my_list = [1, 2, 3]
my_list.extend([4, 5])  # Result: [1, 2, 3, 4, 5]
```

## Searching and Counting
3. `index(x)`: Returns the index of the first occurrence of a specific value in the list.

```
my_list = [1, 2, 3, 2]
index = my_list.index(2)  # Result: 1
```

4. `count(x)`: Returns the number of times a specific value appears in the list.

```
my_list = [1, 2, 3, 2]
count = my_list.count(2)  # Result: 2
```

## Sorting and Reversing
5. `sort()`: Sorts the list in ascending order.

```
my_list = [3, 1, 2]
my_list.sort()  # Result: [1, 2, 3]
```
6. `reverse()`: Reverses the order of elements in the list.

```
my_list = [1, 2, 3]
my_list.reverse()  # Result: [3, 2, 1]
```

## Copying

7. `copy()`: Returns a shallow copy of the list.

```
my_list = [1, 2, 3]
new_list = my_list.copy()  # Result: [1, 2, 3]
```
