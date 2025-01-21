# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user inputs.  Specifically, the provided code attempts to parse a user ID from the request parameters without any validation or error handling. This can lead to unexpected crashes or incorrect responses.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides a corrected version with added error handling to address the issue.

## How to reproduce

1. Clone this repository.
2. Run `npm install express`.
3. Run `node bug.js`.
4. Send a GET request to `/users/abc` (or any non-numeric ID).  Observe the error.
5. Run `node bugSolution.js` and test again with the same request. The solution correctly handles the invalid ID and returns a 404 error.