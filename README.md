# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  Improper use of the dependencies array can lead to an infinite loop, causing performance issues and application crashes.

## Bug Description

The `useEffect` hook in the `bug.js` file is designed to log the current count value. However, omitting the dependency array or including unnecessary dependencies can result in the effect being called excessively, triggering an infinite loop because every render changes the count.

## Solution

The `bugSolution.js` file shows how to correctly implement the `useEffect` hook to avoid this issue.  The dependency array `[count]` ensures that the effect only runs when the `count` state variable changes.

## How to Reproduce

1. Clone the repository
2. Navigate to the project directory
3. Run `npm install`
4. Run `npm start` (assuming you have a suitable React development environment)

Observe the console output in `bug.js` and note the repeated logging. Then compare to `bugSolution.js` to see the effect of using the dependency array correctly.