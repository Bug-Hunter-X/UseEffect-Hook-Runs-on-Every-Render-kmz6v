# React useEffect Hook Runs on Every Render
This repository demonstrates a common mistake when using the `useEffect` hook in React: the effect runs on every render instead of only once on mount.  This can lead to performance issues and unexpected behavior.

## Bug
The provided `MyComponent` uses `useEffect` without a dependency array. This causes the effect to run on every render, logging 'Effect ran!' to the console each time the component updates.  The intended behavior is for the effect to run only once, when the component first mounts.

## Solution
The solution involves adding an empty dependency array `[]` to the `useEffect` hook. This ensures that the effect is executed only once when the component initially mounts.