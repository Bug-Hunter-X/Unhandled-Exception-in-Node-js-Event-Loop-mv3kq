# Unhandled Exception in Node.js Event Loop

This repository demonstrates a common error in Node.js applications: unhandled exceptions in the event loop.  Unhandled exceptions can lead to application crashes or unexpected behavior. This example shows how to identify and handle such exceptions to prevent application failure.

## The Problem

The `bug.js` file contains a simple HTTP server. However, it lacks error handling, making it vulnerable to unhandled exceptions.

## The Solution

The `bugSolution.js` file provides a corrected version with proper error handling using `process.on('uncaughtException')` to gracefully handle unexpected exceptions.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` (this will likely crash or exit prematurely without proper error logging).
4. Run `node bugSolution.js` (this will handle exceptions gracefully and log an error message).