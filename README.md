# Lua pairs Iterator Bug

This repository demonstrates a potential issue with Lua's `pairs` iterator when used with nested tables that are modified during iteration. The bug occurs in the `foo` function, which recursively iterates through a nested table. If a nested table is altered while being iterated, `pairs` might skip elements.

## Reproducing the Bug

1.  Clone this repository.
2.  Run `bug.lua`.  Observe the output.  It may not correctly traverse all elements of the nested table.

## Solution

The solution involves making a copy of the table being iterated over or using an alternative method that won't cause issues with dynamic modifications during iteration.

## Running the Solution

1.  Run `bugSolution.lua` to see the corrected behavior.