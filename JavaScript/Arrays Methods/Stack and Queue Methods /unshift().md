# unshift()

- **Adds one or more elements to the beginning** of an array and returns the new length of the array.

## Usage

```jsx
array.unshift(element1, element2, ..., elementN);
```

## Example

**Example 1:** Adding elements to the beginning of an array

```jsx
let fruits = ['apple', 'banana'];
fruits.unshift('cherry', 'date');
console.log(fruits); // Output: ['cherry', 'date', 'apple', 'banana']
```

**Example 2:** Adding a single element to the beginning of an array

```jsx
let numbers = [3, 4, 5];
numbers.unshift(2);
console.log(numbers); // Output: [2, 3, 4, 5]
```