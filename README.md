# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a peculiar issue encountered when using a catch-all route ("/*") in conjunction with other defined routes within React Router Dom v6.  The catch-all route unexpectedly intercepts requests, even when a more specific route should be handling the navigation.

## Problem

The issue stems from the order and combination of routes.  When a catch-all route (`path="/*"`) is present alongside other specific routes, it often overrides the specific routes' functionality. This leads to the catch-all component being rendered even when a different component should be displayed.

## Solution

The solution is to move the catch-all route to the end of the Routes. This change ensures that React Router Dom properly evaluates the more specific paths before the catch-all. This ensures that the intended component renders for specific paths, and only when no other routes are matched, does the 404 page display.

## Setup

1. Clone the repository.
2. Navigate to the project directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.