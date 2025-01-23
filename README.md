# Stale Closure in useEffect with setInterval

This repository demonstrates a common error in React when using the `useEffect` hook with `setInterval`. The problem arises from using a stale closure over the state variable, resulting in incorrect updates.

## Bug

The `bug.js` file contains a component that attempts to increment a counter every second using `setInterval`. However, the closure over `count` inside `setInterval` captures the initial value of `count`, leading to the counter remaining stuck at 0 or updating erratically.

## Solution

The `bugSolution.js` file provides the corrected implementation. The key change is using the functional update form of `setCount` to ensure that the latest state value is always used.