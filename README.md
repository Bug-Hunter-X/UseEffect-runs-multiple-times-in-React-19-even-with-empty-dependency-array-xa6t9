# React 19 useEffect Bug

This repository demonstrates a subtle bug in React 19 where a useEffect hook with an empty dependency array runs multiple times unexpectedly.  This is particularly problematic because it can lead to performance issues and unexpected behavior.

## Bug Description

The `useEffect` hook, even with an empty dependency array (`[]`), is firing multiple times, leading to unnecessary re-renders and console logs. This contradicts the expected behavior of `useEffect` with an empty array, which should only run once after the initial render.

## Solution

The solution involves ensuring that the component's re-renders are correctly managed and that no unnecessary state updates are triggering the `useEffect` hook.