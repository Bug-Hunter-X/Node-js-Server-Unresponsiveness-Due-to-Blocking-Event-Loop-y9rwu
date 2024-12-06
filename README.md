# Node.js Server Unresponsiveness Due to Blocking Event Loop

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

The server in `bug.js` simulates a long-running task using a `while` loop. This blocks the event loop, preventing it from handling other requests or events.  As a result, the server becomes unresponsive and new requests will time out.

## Solution

The solution in `bugSolution.js` addresses this by using asynchronous operations. This allows the event loop to continue processing events even while the long-running task is executing.  This prevents the server from hanging.