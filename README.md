# React useEffect Hook Optimization

This example demonstrates a common performance issue in React applications involving the `useEffect` hook. The provided `MyComponent` uses `useEffect` without specifying dependencies, causing it to run after every render, leading to unnecessary re-renders and potential performance bottlenecks. The solution shows how to optimize the `useEffect` hook to only run when the `count` state variable changes.

## Bug:
The original code's `useEffect` hook runs after every render, logging the current count to the console. This is inefficient, especially with more complex components and state changes. The console logs will be frequent and potentially cause performance issues.

## Solution:
The optimized code adds a dependency array `[count]` to the `useEffect` hook. This ensures the effect only runs when the value of `count` changes, preventing unnecessary executions.