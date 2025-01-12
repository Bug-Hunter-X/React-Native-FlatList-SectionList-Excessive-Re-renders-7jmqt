# React Native FlatList/SectionList Excessive Re-renders

This repository demonstrates a common performance issue in React Native involving `FlatList` or `SectionList` components: excessive re-renders due to improper `keyExtractor` usage or unnecessary data updates.  The issue manifests as lag, dropped frames, and a generally poor user experience. The `bug.js` file shows the problematic code, while `bugSolution.js` presents the corrected version.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app on a device or emulator.
4. Observe the performance issues in `bug.js`. Note the excessive re-rendering.
5. Compare the performance with `bugSolution.js`. Note the improvement after addressing the `keyExtractor` and ensuring data updates are optimized.

## Solution

The primary solution is to use a proper `keyExtractor` function within the `FlatList` or `SectionList` component. This function ensures that React Native can efficiently identify and update only the necessary items.  Additionally, optimizing data updates to prevent unnecessary re-renders greatly enhances performance.