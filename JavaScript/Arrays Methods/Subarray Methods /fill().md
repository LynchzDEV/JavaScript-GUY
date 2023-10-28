# fill()

- Changes all elements in an array to a static value, from a start index (default 0) to an end index (default `array.length`). It modifies the original array.

## Usage

```jsx
array.fill(value, start, end);
```

Here,

- `value`: The value to fill the array with.
- `start`: Optional. The index to start filling the array. Defaults to 0.
- `end`: Optional. The index to stop filling the array (not inclusive). Defaults to `array.length`.

## Example

**Example 1:** Filling an array with a static value

```jsx
let numbers = [1, 2, 3, 4, 5];
numbers.fill(0);
console.log(numbers); // Output: [0, 0, 0, 0, 0]
```

**Example 2:** Filling a portion of an array with a static value

```jsx
let array = [1, 2, 3, 4, 5];
array.fill(0, 2, 4);
console.log(array); // Output: [1, 2, 0, 0, 5]
```