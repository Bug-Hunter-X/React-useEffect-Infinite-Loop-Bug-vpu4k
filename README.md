# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to an incorrectly defined dependency array.

## Bug Description
The `useEffect` hook is used to perform side effects after rendering. When the dependency array is missing or contains an incorrect list of dependencies, the effect will run on every render, leading to an infinite loop. In this example, the dependency array is missing `count`, causing the effect to constantly re-render and update the count, triggering another execution of the effect.

## How to Reproduce
1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs and the rapid increment of the counter

## Solution
The solution involves adding the `count` variable to the dependency array for the `useEffect` hook. This ensures that the effect only runs when the `count` value changes.
