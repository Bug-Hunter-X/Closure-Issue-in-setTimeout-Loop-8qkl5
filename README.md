# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common closure issue in JavaScript when using `setTimeout` within a loop.  The problem arises because of how closures capture variables.

## Bug Description
The code intends to log numbers 0 through 9 with a 1-second delay between each log. However, due to the closure behavior, it incorrectly logs 10 ten times.

## Solution
The issue is resolved by using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that a unique copy of the `i` variable is captured for each `setTimeout` callback.