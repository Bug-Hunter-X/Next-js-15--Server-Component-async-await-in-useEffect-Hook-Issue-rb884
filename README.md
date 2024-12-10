# Next.js 15 Server Component Async/Await in useEffect Hook Issue

This repository demonstrates an uncommon bug in Next.js 15 related to using server components with `async/await` within a `useEffect` hook in client components.  The issue manifests as unexpected rendering behavior or infinite loading states.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file presents a possible solution.

## Problem
The `async/await` call within `useEffect` in a client component that fetches data from a server component does not correctly integrate with the client-side rendering cycle.  This can cause unpredictable rendering issues.

## Solution
The recommended approach is to refetch the data outside of the `useEffect` hook.  Managing the loading state explicitly ensures proper data handling and rendering.