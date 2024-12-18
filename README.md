# React useEffect Cleanup Function Missing

This example demonstrates a common error in React's `useEffect` hook: omitting the cleanup function.  This can lead to memory leaks and unexpected behavior, particularly when fetching data or managing subscriptions.

## Bug
The `bug.js` file shows a component that fetches data on mount using `useEffect`.  However, it lacks a cleanup function to cancel the fetch request if the component unmounts before the request completes. This can result in wasted resources and potential race conditions.

## Solution
The `bugSolution.js` file provides the corrected code.  A cleanup function is added to the `useEffect` hook. This function is executed when the component unmounts, ensuring that any ongoing requests are cancelled, preventing memory leaks and unexpected behavior.