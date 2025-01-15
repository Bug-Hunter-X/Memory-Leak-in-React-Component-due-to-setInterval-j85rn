# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks because the interval continues to run even after the component unmounts.

## Bug
The `bug.js` file shows the faulty component.  `setInterval` is used without the return function to clear the interval. 

## Solution
The `bugSolution.js` file provides the corrected implementation that uses a cleanup function within the `useEffect` hook to clear the interval before the component unmounts, thus preventing memory leaks. 