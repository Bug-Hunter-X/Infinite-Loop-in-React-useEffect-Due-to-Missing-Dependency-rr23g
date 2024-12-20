# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array. 

## Bug Description
The `useEffect` hook, when used without specifying a dependency array, or with an incomplete dependency array, executes on every render. This can lead to infinite render loops, especially if the effect modifies state or props that trigger re-renders.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console; you'll see the count logging infinitely.

## Solution
The solution involves correctly specifying the dependency array.  In this case, the `count` variable needs to be included in the dependency array so that useEffect only runs when `count` changes.