# Infinite Re-renders in React useEffect Hook

This repository demonstrates a common React bug: infinite re-renders caused by a missing dependency array in the `useEffect` hook.

## Bug Description
The `MyComponent` continuously re-renders because the `useEffect` hook lacks a dependency array.  This causes the effect to run after every render, creating a loop. The console shows the message 'Component rendered' repeatedly.

## Solution
The solution involves adding a dependency array to the `useEffect` hook. This array specifies which values the effect depends on. The effect will only run when these values change. In this case, the effect only needs to run when `count` changes, so `[count]` is the dependency array.