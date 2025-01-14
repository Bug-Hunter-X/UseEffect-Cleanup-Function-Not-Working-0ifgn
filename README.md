# React useEffect Cleanup Function Issue

This repository demonstrates a problem with the cleanup function in React's `useEffect` hook.  The expected behavior is that the cleanup function should execute when the component unmounts.  However, in this example, the cleanup function is not working correctly.

## Bug Description:

The `useEffect` hook is used to log 'Mounted!' when the component mounts and 'Unmounted!' when it unmounts.  The 'Mounted!' message is logged correctly, but the 'Unmounted!' message is not logged when the component is unmounted.

## How to Reproduce:

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console logs.  You'll see 'Mounted!', but not 'Unmounted!'.
5. Try unmounting the component (e.g., navigating away from the page if it is in a router). The 'Unmounted!' log will not appear. 

## Solution:

The solution involves ensuring that the `useEffect` hook and its cleanup function are correctly implemented and that there are no other conflicting events preventing the component from unmounting or the cleanup function from firing.