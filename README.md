# Off-by-One Error in C++ Vector Iteration

This repository demonstrates a common off-by-one error when iterating over a `std::vector` in C++.  The error arises from an incorrect loop condition that leads to accessing an element beyond the vector's bounds.

## The Bug

The `bug.cpp` file contains a loop that iterates from 0 up to and including `vec.size()`.  This results in accessing `vec[5]` when the vector only has 5 elements (indices 0-4). This causes undefined behavior, often resulting in a crash or incorrect results.

## The Solution

The `bugSolution.cpp` file corrects the loop condition to `i < vec.size()`. This ensures that the loop iterates through all valid indices of the vector, preventing the out-of-bounds access.

## How to Reproduce

1. Clone this repository.
2. Compile and run `bug.cpp` (expect undefined behavior).
3. Compile and run `bugSolution.cpp` (expect correct output).
