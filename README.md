# Unhandled Promise Rejection in Express.js Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous route handlers.  Failure to properly handle errors within asynchronous operations can lead to unexpected crashes and a poor user experience.

## Bug

The `bug.js` file contains an Express.js server with a route handler that performs an asynchronous operation.  However, it lacks proper error handling for the promise rejection.  This results in an uncaught exception and server termination.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle potential errors within asynchronous route handlers.  Using a `.catch()` block within the promise chain allows the server to gracefully manage exceptions without crashing.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js`. Observe the server crashes.
4. Run `node bugSolution.js`. Observe the server handles the error gracefully and continues running.