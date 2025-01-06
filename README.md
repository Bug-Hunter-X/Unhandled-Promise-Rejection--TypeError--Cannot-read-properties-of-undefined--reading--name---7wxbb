# React Native: Accessing State Before Initialization

This repository demonstrates a common error in React Native: attempting to access state or props before they have been fully initialized.  This often occurs when dealing with asynchronous operations.

## Problem
The code in `bug.js` attempts to render data from an API call before the data has been fetched and set to the state. This results in a `TypeError: Cannot read properties of undefined (reading 'name')` error.

## Solution
The `bugSolution.js` file provides a corrected version.  It uses the optional chaining operator (`?.`) to safely access properties and handles the case where data might be null or undefined.