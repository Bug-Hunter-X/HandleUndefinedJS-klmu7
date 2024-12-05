# JavaScript Null and Undefined Handling Bug

This repository demonstrates a common bug in JavaScript related to handling null and undefined values.  The function `foo` intends to add two numbers but fails to gracefully handle cases where one or both inputs are undefined.

## Bug Description

The function correctly handles null values, returning null if either `a` or `b` is null. However, if either input is `undefined`, it results in `NaN` instead of the desired behavior (returning null or handling undefined like null).

## How to Reproduce

1. Clone the repository.
2. Run `bug.js` using a JavaScript runtime (like Node.js).
3. Observe the output.  You'll see that `foo(undefined, 2)` returns `NaN`, not null.

## Solution

The solution involves explicitly checking for `undefined` values in addition to `null` values. The `bugSolution.js` file provides a corrected implementation.

## Learning Points

- JavaScript's null and undefined values are distinct and need to be handled separately.
- Consider edge cases (null, undefined) when writing functions.
- Thorough testing is essential to uncover unexpected behavior.