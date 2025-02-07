# Asynchronous Updates in React's useState Hook

This example demonstrates a common pitfall in React when working with the `useState` hook: asynchronous updates.

The `useState` hook updates asynchronously.  If you attempt to access the updated state immediately after calling `setCount`, you'll receive the previous value.

**bug.js** shows the issue. **bugSolution.js** offers a solution using functional updates and useEffect to observe the updated value.

## How to reproduce

1.  Clone this repository.
2.  Run `npm install` to install dependencies.
3.  Run `npm start` to start the development server.
4.  Click the button and observe the console output. The first console.log statement will reflect the updated count while the second one will reflect the previous count.

## Solution

Using functional updates and useEffect to observe the updated value provides a reliable way to work with asynchronous updates. This ensures that your component's state is always up to date and consistent.