# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook.  The bug arises from updating state within the `useEffect` callback without specifying dependencies, leading to continuous re-renders and a performance issue.  The solution showcases how to properly manage dependencies to prevent this issue.

## Bug Description
The `bug.js` file contains a React component (`MyComponent`) that uses the `useEffect` hook to increment a counter. Because the `useEffect` hook doesn't have any dependencies, it runs on every render, updating the count and subsequently triggering another render, resulting in an infinite loop.

## Solution
The `bugSolution.js` file provides a corrected version. By adding `count` as a dependency to the `useEffect` hook, the hook only runs when the `count` value changes. This effectively breaks the infinite loop and ensures the component renders correctly.