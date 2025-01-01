# Unresponsive Node.js Server Due to Synchronous Long-Running Task

This repository demonstrates a common Node.js issue where a long-running synchronous operation blocks the event loop, making the server unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Bug

The server simulates a long-running task (5-second busy wait) within the request handler.  During this time, the server cannot process any other requests, leading to unresponsiveness.

## Solution

The solution involves using asynchronous operations, allowing the event loop to continue processing other requests while the long-running task executes in the background.

## How to Run

1. Clone the repository.
2. Run `node bug.js` to observe the unresponsive server behavior.
3. Run `node bugSolution.js` to see the solution in action.