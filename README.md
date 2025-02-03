# Uncommon React useEffect Memory Leak

This repository demonstrates a subtle memory leak in a React component that uses `setInterval` within the `useEffect` hook without proper cleanup.  The bug arises from forgetting to clear the interval when the component unmounts, leading to continuous counter updates even after the component is no longer visible.