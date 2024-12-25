# React Native: Multiple Re-renders Before Async Operation Completion

This repository demonstrates a common bug in React Native applications where components re-render multiple times before asynchronous operations (like API calls) complete, leading to unexpected behavior and potential race conditions.  The bug and its solution are presented in separate JavaScript files.

## Bug (`bug.js`)

The `bug.js` file contains a component that attempts to update its state with data fetched asynchronously.  Due to the multiple renders before the data arrives, the app can exhibit unpredictable behavior.

## Solution (`bugSolution.js`)

The `bugSolution.js` file provides a corrected version of the component.  It uses techniques like `useEffect` with the cleanup function or asynchronous functions to prevent unnecessary renders and race conditions.

## How to reproduce:

1. Clone the repository.
2. Navigate to the directory in your terminal.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the behavior of the app.