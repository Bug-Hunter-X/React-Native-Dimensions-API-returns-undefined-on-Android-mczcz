# React Native Dimensions Bug

This repository demonstrates a common bug encountered when using the `Dimensions` API in React Native on Android. The problem arises because the dimensions are not immediately available when the component mounts, leading to undefined values or errors.

## Bug
The `DimensionsBug.js` file showcases the issue. When the component renders, it attempts to use the dimensions provided by `Dimensions.get('window')` immediately. On Android, this often results in `undefined` values for `width` and `height`, causing layout problems or crashes.

## Solution
The `DimensionsBugSolution.js` file demonstrates a solution using the `useEffect` and `useState` hooks. The dimensions are fetched asynchronously using `useEffect`, and `useState` is used to store the dimensions once they are available. This ensures that the component doesn't render with undefined values, preventing errors and ensuring correct layout.