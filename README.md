# JavaScript Closure Issue in `setTimeout`

This example demonstrates a common closure issue in JavaScript loops when using `setTimeout` or similar asynchronous functions.

## Problem

The `myFunction` uses a loop and `setTimeout` to log values. It might be expected that values 0 through 9 should be printed sequentially, but instead, the number 10 is printed ten times. This is because closures do not capture the value of `i` at each iteration. By the time `setTimeout` executes, the loop has already completed, and `i` holds its final value.