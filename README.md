# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where the server becomes unresponsive due to a long-running operation blocking the event loop.  The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The original `server.js` uses a `while` loop to simulate a 5-second delay.  During this time, the server cannot handle any other requests, resulting in a hang.

## Solution

The solution in `serverSolution.js` uses asynchronous operations with `setTimeout` to avoid blocking the event loop.  The server can now handle multiple requests concurrently without hanging.