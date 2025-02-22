# Express.js Route Handler: Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.

Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for errors. If a non-numeric ID is provided, `parseInt(userId)` will return `NaN`, leading to a crash.

The `bug.js` file contains the erroneous code. The `bugSolution.js` file provides a corrected version with proper error handling.

## How to reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install express` to install the required dependencies.
4. Run `node bug.js` and access `/users/abc` in your browser.  Observe the server error. 
5. Run `node bugSolution.js` and access `/users/abc`. Observe the graceful error response.