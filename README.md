# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input.  Specifically, this example shows a route that retrieves a user by ID.  If the ID is not a valid number, the application will crash.  The solution shows how to add proper error handling to prevent this.

## Bug
The `bug.js` file contains the buggy code.  It attempts to parse the user ID as an integer without checking if it's a valid number.  This can lead to a crash if the ID is not a number.

## Solution
The `bugSolution.js` file provides the corrected code. It includes error handling that checks if the user ID is a number before parsing it.  If the ID is not a number, it returns a 400 Bad Request response.  If the user is not found, it returns a 404 Not Found response.