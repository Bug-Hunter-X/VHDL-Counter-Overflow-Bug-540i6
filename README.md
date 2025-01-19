# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: integer overflow in a counter. The provided `buggy_counter.vhdl` code implements a simple counter that increments with every clock cycle. However, it does not handle the case when the counter reaches its maximum value.  The `buggy_counter_fixed.vhdl` file shows a corrected implementation.

## Bug Description
The `buggy_counter.vhdl` code lacks proper handling of the counter reaching its maximum value (15 in this case). When the counter reaches 15, the next increment will lead to an overflow and undefined behavior.  This could result in unexpected outputs or even simulation errors.

## Solution
The `buggy_counter_fixed.vhdl` provides a corrected version which uses a modulo operator to handle the overflow gracefully. When the counter reaches 15, it wraps back to 0.
