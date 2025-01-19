# Express.js Route Handler Error

This repository demonstrates a common error in Express.js route handlers: lack of error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without validating it, leading to potential issues if the parameter is not a valid integer.

## Bug

The `bug.js` file contains the erroneous code.  It tries to find a user by ID, but fails to handle cases where the ID is not a number, resulting in unexpected behavior or crashes.

## Solution

The `bugSolution.js` file shows the corrected code. It adds input validation to ensure that the `userId` is a valid integer before attempting to use it to find a user.  It includes error handling to return a 404 status code if the user is not found.