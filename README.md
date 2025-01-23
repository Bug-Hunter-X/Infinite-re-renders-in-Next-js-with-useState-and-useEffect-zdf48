# Next.js Infinite Re-renders Bug
This repository demonstrates a common bug in Next.js applications involving infinite re-renders when using `useState` and `useEffect` hooks together.  The issue arises from a combination of data fetching and state updates within a component, leading to an unexpected loop that prevents the application from rendering properly.

## Bug Description
The bug occurs when a component's state is updated within a `useEffect` hook while simultaneously relying on data fetched from an API.  This creates a situation where the component re-renders continuously, resulting in an infinite loop of updates. This is particularly problematic in applications that handle complex data transformations or external API calls within their components.

## Solution
The problem is solved using a more controlled approach to data fetching and state updates.  We can use techniques to manage updates efficiently such as the `useCallback` hook to prevent re-renders when unnecessary.