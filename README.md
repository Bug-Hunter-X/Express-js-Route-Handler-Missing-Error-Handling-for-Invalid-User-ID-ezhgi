# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  the lack of proper error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for errors.  If a non-numeric ID is provided, the application may crash or return unexpected results.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file provides a corrected version with improved error handling, including input validation and more robust error responses.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `node bug.js` and navigate to `/users/abc` in your browser or using a tool like `curl`.  Observe the error.
4. Run `node bugSolution.js` and repeat step 3.  The improved error handling will provide a more graceful response.