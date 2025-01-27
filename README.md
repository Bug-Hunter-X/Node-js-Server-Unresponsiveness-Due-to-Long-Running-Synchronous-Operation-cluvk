# Node.js Server Unresponsiveness Bug

This repository demonstrates a common issue in Node.js where a long-running synchronous operation within the request handler causes the server to become unresponsive.  The bug is in `bug.js`, and the solution is provided in `bugSolution.js`.

**Problem:** The server hangs for 5 seconds before responding. During that time, it cannot handle any other requests.

**Solution:**  Refactor the long-running task to be asynchronous, preventing the event loop from blocking.

This example highlights the importance of using asynchronous operations in Node.js server applications to maintain responsiveness and prevent performance issues.