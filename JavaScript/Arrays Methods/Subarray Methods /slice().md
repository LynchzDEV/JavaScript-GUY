# slice()

- Extracts a section of an array and returns a new array without modifying the original one.

## Usage

```jsx
let newArray = array.slice(start, end);
```

Here,

- `start`: The beginning index at which to begin extraction.
- `end`: The ending index before which to end extraction. The extracted portion will go up to, but not including, the element at this index.

## Example

**Example 1:** Slicing elements from an array

```jsx
let fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry'];
let slicedFruits = fruits.slice(1, 4);
console.log(slicedFruits); // Output: ['banana', 'cherry', 'date']
```

**Example 2:** Slicing elements from the end of an array

```jsx
let numbers = [1, 2, 3, 4, 5];
let slicedNumbers = numbers.slice(-3);
console.log(slicedNumbers); // Output: [3, 4, 5]
```