# Tcl Type-Sensitive Comparison Bug

This repository demonstrates a subtle bug in Tcl related to its type-sensitive comparison using the `==` operator. When comparing values of different numeric types (e.g., integer and floating-point), the `==` operator returns false even if the values are numerically equivalent.

## Bug Description

The `badproc` procedure compares two arguments using `==`. If the arguments are numerically the same but of different types (integer vs. floating-point), the comparison fails unexpectedly.

## Bug Reproduction

1.  Clone this repository.
2.  Run `tclsh bug.tcl`. The output will be 0, indicating that 1 and 1.0 are considered unequal by `==`.

## Solution

The `bugSolution.tcl` file provides a corrected version of the procedure using the `==` operator to perform type insensitive comparison.