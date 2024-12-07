# F# Mutable Variable Bug

This repository demonstrates a common error in F# involving the unexpected behavior of mutable variables within a function.  The `add` function modifies its input parameters, resulting in behavior that may not be intuitive to developers unfamiliar with F#'s handling of mutable variables.

## The Problem
The code in `bug.fs` demonstrates how using mutable variables directly as function inputs can lead to subtle bugs. Changes made inside the `add` function permanently affect the variables passed into the function. This can lead to unexpected values in subsequent calculations.

## The Solution
The `bugSolution.fs` file provides a corrected version. It avoids the problem by making copies of the inputs before performing operations.

This example highlights the importance of careful consideration when using mutable variables, especially as function parameters, in F#.