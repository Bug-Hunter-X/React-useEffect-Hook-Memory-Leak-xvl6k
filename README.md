# React useEffect Hook Memory Leak

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include a cleanup function to prevent memory leaks.  Specifically, the example shows an `setInterval` that continues to run even after the component unmounts. 

## How to reproduce the bug:

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter incrementing even after unmounting the component.

## How to fix the bug:

The solution involves adding a return statement to the `useEffect` function. This return statement should contain a function that clears the interval when the component is unmounted. See `bugSolution.js` for the corrected code.