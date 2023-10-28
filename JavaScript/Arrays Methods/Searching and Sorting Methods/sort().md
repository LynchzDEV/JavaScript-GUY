# sort()

- Sorts the elements of an array in place and returns the sorted array.
- The default sort order is ascending, built upon converting elements into strings and comparing their sequences of UTF-16 code units.

## Usage

```jsx
array.sort(compareFunction);
```

## Example

**Example 1:** Sorting strings in alphabetical order

```jsx
let fruits = ['banana', 'cherry', 'apple', 'date'];
fruits.sort();
console.log(fruits); // Output: ['apple', 'banana', 'cherry', 'date']
```

**Example 2:** Sorting numbers in ascending order

```jsx
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5];
numbers.sort(function (a, b) {
  return a - b;
});
console.log(numbers); // Output: [1, 1, 2, 3, 4, 5, 5, 6, 9]
```

**Example 3:** Sorting in a case-insensitive manner

```jsx
let myArray = ["Apple", "banana", "Orange", "cherry"];
myArray.sort(function (a, b) {
  return a.toLowerCase().localeCompare(b.toLowerCase());
});
console.log(myArray); // Output: ["Apple", "banana", "cherry", "Orange"]
```