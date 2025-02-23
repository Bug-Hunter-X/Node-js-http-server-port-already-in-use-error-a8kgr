# Node.js http server port already in use error

This repository demonstrates a common error in Node.js when creating an HTTP server: the `EADDRINUSE` error, which occurs when the specified port is already in use.  The `bug.js` file contains the problematic code, and `bugSolution.js` provides a solution.

## Problem

The `bug.js` file attempts to create an HTTP server on port 8080. If another process (e.g., another instance of the application or a different service) is already using this port, the server will fail to start and throw an error.

## Solution

The `bugSolution.js` file demonstrates a robust solution to this problem by checking if the port is available before attempting to bind to it. It uses a `setTimeout` function to retry connecting to the port after a short delay if an error occurs.