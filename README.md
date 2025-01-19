# Unexpected String Concatenation in JavaScript

This repository demonstrates a common yet subtle bug in JavaScript stemming from its loose typing system. The `foo` function intends to add two numbers, but due to implicit type coercion, it concatenates strings when a number and a string are passed as arguments. 

## Bug Description
The `foo` function should perform numeric addition. However, when one argument is a number and the other is a string, JavaScript converts the number to a string and performs string concatenation rather than numerical addition. This leads to an unexpected result.

## How to Reproduce
1. Clone this repository.
2. Run `bug.js` using a JavaScript runtime (like Node.js).
3. Observe that the output is '55' instead of the expected 10.

## Solution
The `bugSolution.js` file provides a corrected version of the `foo` function that explicitly converts both arguments to numbers before performing addition, thereby avoiding the unintended string concatenation.