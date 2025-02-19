# React useEffect Hook: Missing Dependency Causes Infinite Loop

This repository demonstrates a common React bug involving the `useEffect` hook.  The issue stems from an improperly defined dependency array, resulting in an infinite rendering loop.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.

## Bug Description

The `useEffect` hook in `bug.js` lacks a dependency array, causing it to run after every render. This continuous execution leads to a recursive loop and often causes performance issues or crashes.  The console will repeatedly log 'Effect running!', demonstrating the unintended behavior.

## Solution

The solution in `bugSolution.js` addresses this by adding `count` to the dependency array. Now, the `useEffect` hook only runs when the value of `count` changes, preventing the infinite loop.