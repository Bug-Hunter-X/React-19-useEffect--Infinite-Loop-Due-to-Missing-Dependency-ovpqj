# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common error in React 19's `useEffect` hook: an infinite loop caused by omitting a state variable from the dependency array.  The `bug.js` file shows the erroneous code, while `bugSolution.js` provides the corrected version.

## Bug Description

The original code incorrectly omits `count` from the dependency array of the `useEffect` hook.  This leads to the effect running on every render, constantly updating the `count` state and triggering another render, resulting in an infinite loop. 

## Solution

The solution involves adding `count` to the dependency array. This ensures that the effect only runs when the `count` value changes.