# React Router v6 Strict Matching Bug

This repository demonstrates a common issue encountered when using React Router v6: unexpected behavior when navigating to undefined routes due to strict matching.  The bug occurs because the routes are not handling cases where a user navigates to a path that doesn't have an explicitly defined route.  This often results in a blank screen or an application that appears to be stuck loading.

The `bug.js` file contains the buggy implementation.  The `bugSolution.js` file shows a solution using a `Route` component with a wildcard path (`/*`) to catch all undefined routes.  This prevents the application from crashing or showing a blank screen.

## How to reproduce the issue

1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `npm install`.
4. Run `npm start`.
5. Navigate to a non-existent route, such as `/nonexistent` in the browser.

You will observe that the application will not display anything for this route. This is the bug.

## Solution

The solution adds a catch-all route to handle cases where the route is not found.