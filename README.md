# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an incorrect dependency array, leading to an infinite loop. The solution shows how to fix it.

## Bug Description
The `useEffect` hook is used to perform side effects in functional components. In this example, it attempts to increment a counter every second. However, because the dependency array is empty (`[]`), the effect runs on every render, causing `setCount` to be called repeatedly. This creates an infinite loop that slows down the application and consumes excessive resources. 

## Solution
The solution involves including `count` in the dependency array. This ensures the effect only runs when the value of `count` changes.