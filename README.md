# React Router v6 Catch-All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router v6. The problem arises when this route interferes with other, more specific routes, unexpectedly overriding their rendering.

## Problem

The `path="/*"` route, intended to handle 404 errors, incorrectly captures all routes, even if a valid route exists.  This leads to the catch-all component (`NotFound` in this case) being displayed regardless of the URL.

## Solution

The issue is resolved by carefully ordering the routes.  More specific routes should always be defined *before* the catch-all route to ensure that they are matched correctly.  The catch-all route should be placed last. This example showcases a correct implementation.