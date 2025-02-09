# React Router Catch-all Route Conflict

This repository demonstrates a common issue with React Router's catch-all route (`path="/*"`) when placed before other routes. The catch-all route unintentionally captures all other routes, leading to unexpected rendering.

## Bug
The provided `App.js` demonstrates how the catch-all route (`path="/*"`) placed before other routes results in the `NotFound` component always being rendered.  Even navigating to paths such as `/about` will trigger the `NotFound` component.

## Solution
The `AppSolution.js` provides the corrected implementation where the catch-all route is placed last within the `<Routes>` component. This ensures that specific routes are matched first and only if none of the specific routes match does the catch-all route take effect.