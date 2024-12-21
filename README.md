# Unhandled Error in Asynchronous Node.js Express.js Server

This repository demonstrates a common error in Node.js Express.js servers: unhandled errors within asynchronous operations.  When an error occurs within an asynchronous callback (like `setTimeout` in this case), if it's not properly caught, it can lead to the server crashing unexpectedly.

The `bug.js` file showcases this issue. The `bugSolution.js` file provides a solution by implementing proper error handling.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js`.
4. Observe the server's behavior (it will crash if the random number is >= 0.5).
5. Then run `node bugSolution.js`, it will not crash the server even if it encounters an error.

## Solution

The solution involves using `try...catch` blocks or error handling middleware within the asynchronous operation to gracefully handle errors and prevent the server from crashing. The solution is demonstrated in `bugSolution.js`.