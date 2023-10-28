# indexOf()

- Returns the first index at which a given element can be found in the array, or -1 if it is not present.

## Usage

```jsx
let index = array.indexOf(element, start);
```

Here,

- `element`: The element to locate in the array.
- `start`: Optional. The index at which to start the search. If omitted, the search starts from index 0.

## Example

**Example 1:** Finding the index of an element in an array

```jsx
let fruits = ['apple', 'banana', 'cherry', 'date'];
let index1 = fruits.indexOf('cherry');
console.log(index1); // Output: 2
```

**Example 2:** Finding the index of an element with a specified starting point

```jsx
let numbers = [2, 5, 9, 2];
let index2 = numbers.indexOf(2, 2);
console.log(index2); // Output: 3
```