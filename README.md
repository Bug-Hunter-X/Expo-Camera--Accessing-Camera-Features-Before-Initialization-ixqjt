# Expo Camera Initialization Issue

This repository demonstrates a common error when working with the Expo Camera API: attempting to use camera features before the camera has fully initialized.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected implementation.

## Problem

The issue stems from accessing camera properties or functions before the camera is ready. This can result in silent failures (no preview, no functionality) or explicit errors related to an undefined camera object.

## Solution

The solution involves using the `cameraRef` and its `current` property in conjunction with a state variable to ensure the camera is ready before attempting to access it.  The `isReady` state variable tracks initialization, preventing premature access. 