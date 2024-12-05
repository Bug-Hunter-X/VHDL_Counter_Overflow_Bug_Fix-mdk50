# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL: an integer counter without proper overflow handling.  The original `counter.vhdl` code increments an integer until it reaches its maximum value. Upon reaching 15, the next increment will result in unexpected behavior (wrapping or other undefined results) because the integer type does not have a mechanism to handle the overflow naturally.  The improved `counter_fixed.vhdl` shows a solution.

## Bug Description

The `counter.vhdl` VHDL code implements a simple counter. However, it lacks explicit overflow protection. When the counter reaches its maximum value (15), the next increment results in undefined behavior.  This is a common error in VHDL when using integer types without proper checks.

## Solution

The `counter_fixed.vhdl` code addresses this by adding a conditional statement to check for the maximum count before incrementing. This prevents overflow and ensures predictable behavior.