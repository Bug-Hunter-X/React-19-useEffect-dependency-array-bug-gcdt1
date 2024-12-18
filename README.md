# React 19 useEffect Dependency Array Bug

This repository demonstrates a common but subtle bug in React 19 related to the `useEffect` hook's dependency array. The example shows how an incorrect dependency array can lead to unexpected behavior where an effect doesn't update when it should.

## Bug Description
The `useEffect` hook is meant to perform side effects after rendering.  However, if the dependency array is empty (`[]`), the effect will run only once after the initial render and will not run again, even if component state changes. This issue is present in React 19 and earlier versions.

## Solution
To fix this, the `count` state variable must be added to the dependency array.  This tells React to re-run the effect whenever the `count` value changes.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe that the console log only runs once, even after clicking the button to increment the count.

## How to fix
Examine the `bugSolution.js` file for the corrected code.