# React Router Dom Catch-All Route Issue

This repository demonstrates an uncommon bug in React Router Dom v6 related to the catch-all route ('/*').  The issue arises when a catch-all route is defined after other specific routes.  Even if a URL matches one of the specific routes, the catch-all route may still be triggered, preventing other components from rendering correctly.  This issue is subtle and may not manifest in simple applications.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/` or `/about`.  Notice that the catch-all route still renders, instead of the Home or About component.

## Solution

The solution involves carefully ordering the routes in the `Routes` component. The catch-all route should always be the last one defined. This example demonstrates the correct order and resolves the issue.