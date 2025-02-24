# React setInterval Memory Leak
This repository demonstrates a common error in React applications involving the `setInterval` function within the `useEffect` hook.  The example showcases how forgetting to return a cleanup function from `useEffect` leads to a memory leak. The solution provides the correct implementation with proper cleanup. 

## Problem
The `setInterval` function, if not handled correctly inside `useEffect`, will continue running even after the component unmounts. This results in the creation of unnecessary intervals and leads to memory leaks, especially in components that render and unrender frequently.  The provided `bug.js` illustrates this issue.