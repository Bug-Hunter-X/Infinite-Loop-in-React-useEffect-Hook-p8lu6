# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite loop.  The bug arises from incorrectly specifying the dependency array, leading to an infinite render cycle.

## Bug Description

The `MyComponent` uses `useEffect` to update the `count` state.  However, because the `count` state is updated within the `useEffect` and  the dependency array `[]` is empty, this creates an infinite loop, as the effect runs again and again after every render.