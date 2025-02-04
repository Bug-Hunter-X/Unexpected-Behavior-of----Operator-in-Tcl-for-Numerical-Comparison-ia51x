# Tcl == Operator Numerical Comparison Bug

This repository demonstrates a common error in Tcl involving the use of the `==` operator for comparing numbers.  Because Tcl's `==` performs string comparison, numerical comparisons might produce unexpected results.

## Bug Description
The provided `badproc` procedure intends to compare two numbers and return 1 if they are equal, 0 otherwise. However, because it uses `==`, it does string comparison instead, leading to incorrect results.

## How to Reproduce
1.  Save the code in `bug.tcl`.
2.  Run the script using `tclsh bug.tcl`.
3. Observe the incorrect output.

## Solution
The solution employs the `expr` command to perform numerical comparison.

## Additional Notes
Always use `expr` for numerical comparisons in Tcl to avoid these common pitfalls.  Understanding the distinction between string and numerical comparisons is crucial for writing robust Tcl code.