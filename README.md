# Lua Nested Table Iteration Issue

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with nested tables. The `pairs` function does not guarantee a specific iteration order, which can lead to unexpected results if the order of processing is important.

## The Problem

The `bug.lua` file contains a function `foo` that recursively iterates through a nested table using `pairs`. Because `pairs` doesn't guarantee order, the processing sequence is not consistent across different Lua implementations or even runs.

## The Solution

The `bugSolution.lua` file offers a solution that uses a different approach to ensure consistent iteration order. This ensures that the processing sequence remains the same regardless of the Lua implementation or the specifics of the system.

## How to Reproduce

1. Clone this repository.
2. Run `bug.lua` multiple times. Observe the inconsistent order of processing.
3. Run `bugSolution.lua`. Observe the consistent order of processing.

This example highlights the importance of considering the implications of `pairs`'s unordered iteration when working with nested tables in Lua.