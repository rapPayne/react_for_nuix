# Testing JavaScript functions

In this lab, you'll exercise vitest to test JavaScript functions.

## Installation
- Install vitest: `npm install --save-dev vitest`
- Add a test script to your `package.json`
- Run `npm run test` to ensure everything is set up correctly. You should see a message indicating that no tests were found.

## Write a smoke test
- Create a new file with a `.test.js` extension.
- In it, put a simple smoke test that checks if `true` is `true`.

## Putting a few existing functions under test
You probably have some functions in your codebase that make requests from a server. Please save those for later. But you might have some utility functions that are synchronous. You can start by writing tests for those.
- Pick a few functions and create a test file for each of the source files.
- Write tests for each of the functions. Make sure to cover edge cases.
- Run your tests and ensure they pass.

## Test-driven development
For this exercise, please use pair programming, switching roles every major step (where steps are red, green, refactor).

- Identify a synchronous function that you can refactor, perhaps extracting some logic from a component.
- Write tests for the existing behavior of the function.
- Run the tests to ensure they fail.
- Implement the new functionality.
- Run the tests to ensure they pass.
- Refactor the function to improve its design or performance.
- Run the tests to ensure they still pass.
