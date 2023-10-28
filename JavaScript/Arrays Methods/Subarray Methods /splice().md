# splice()

- Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

## Usage

```jsx
array.splice(start, deleteCount, item1, item2, ...);
```

Here,

- `start`: The index at which to start changing the array.
- `deleteCount`: An integer indicating the number of old array elements to remove.
- `item1, item2, ...`: The elements to add to the array.

## Example

**Example 1:** Removing elements from an array

```jsx
let fruits = ['apple', 'banana', 'cherry', 'date'];
let removedItems = fruits.splice(1, 2);
console.log(removedItems); // Output: ['banana', 'cherry']
console.log(fruits); // Output: ['apple', 'date']
```

**Example 2:** Adding elements to an array

```jsx
let numbers = [1, 2, 3, 7, 8, 9];
numbers.splice(3, 0, 4, 5, 6);
console.log(numbers); // Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]
```