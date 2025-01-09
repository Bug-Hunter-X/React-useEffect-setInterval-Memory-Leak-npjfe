# React useEffect setInterval Memory Leak
This example demonstrates a common mistake when using setInterval within a React component's useEffect hook: forgetting to include a cleanup function to clear the interval when the component unmounts. This leads to a memory leak, as the interval continues to run even after the component is removed from the DOM.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to increment a counter every second. However, it's missing a cleanup function in the `useEffect` hook to stop the interval when the component is unmounted. This causes the interval to persist, leading to a memory leak.

## Solution
The `bugSolution.js` file corrects this issue by adding a cleanup function that calls `clearInterval` to stop the interval before the component unmounts.  This prevents the memory leak.