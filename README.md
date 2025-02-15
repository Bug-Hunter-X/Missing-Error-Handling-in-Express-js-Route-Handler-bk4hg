# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The bug involves attempting to parse a user ID as an integer without checking if the input is actually numeric.  This can result in unexpected behavior or crashes.

## Bug Description
The `users/:id` route attempts to retrieve a user based on the provided ID. However, it lacks error handling for cases where the ID is not a valid integer. This can lead to exceptions and application crashes if a non-numeric ID is provided.

## Solution
The solution introduces proper error handling by checking if the ID is a valid integer before attempting to use it. A 404 Not Found status code is returned if the user is not found or the ID is invalid.