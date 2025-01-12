# React useEffect Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and missing dependencies.  The bug leads to unexpected re-renders and potentially infinite loops.

## Bug Description
The `useEffect` hook in the `bug.js` file is missing a dependency, leading to the effect running after every render, even when the `count` state doesn't change. This causes an infinite loop, spamming the console and potentially impacting performance.

## Solution
The `bugSolution.js` file provides a corrected version.  The missing dependency (`count`) is explicitly added to the dependency array, ensuring the effect only runs when `count` changes.

## How to Reproduce
1. Clone this repository.
2. Navigate to the `bug` directory.
3. Run `npm install` (or `yarn install`).
4. Run `npm start` (or `yarn start`).

Observe the console output and the behavior of the counter.  Compare this to the solution.

## Key Learning
Always include all dependencies in the `useEffect` dependency array to avoid unexpected behavior and performance issues. Forgetting to include state variables or other values used within your `useEffect` function's logic is a common source of difficult-to-debug problems.