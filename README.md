# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug involving the `useEffect` hook causing unnecessary re-renders.  The `useEffect` hook in `bug.js` runs after every render, leading to excessive logging and potential performance issues. The solution, provided in `bugSolution.js`, demonstrates how to optimize the `useEffect` hook to only run when the `count` state variable changes, thus improving performance.

## Bug
The bug lies within the `useEffect` hook.  Without dependency array, the effect function runs after every render, even if the value of `count` hasn't changed. This leads to repeated console logs and unnecessary work.

## Solution
The solution involves adding a dependency array to the `useEffect` hook. The dependency array `[count]` ensures that the effect only runs when the value of `count` changes. This significantly improves performance by preventing unnecessary re-renders and computations.