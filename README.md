# Express.js - Missing Error Handler for Non-Numeric User IDs

This repository demonstrates a common error in Express.js applications: missing error handling for invalid user IDs.

## Bug

The `bug.js` file contains an Express.js route that fetches a user by ID.  However, it lacks proper error handling if the ID is not a number.  This can result in crashes or unexpected behavior.  The code attempts to parse a non-numeric string with `parseInt`, which will return `NaN`, leading to the failure to find a user.

## Solution

The `bugSolution.js` file provides a solution by adding input validation to ensure the user ID is a number. It checks for valid numeric input before attempting to find the user. This prevents errors resulting from malformed requests.   Additional error handling is included to return informative error responses to the client in case of invalid input or a missing user.