# VHDL Counter Overflow Bug
This repository demonstrates a common but subtle bug in VHDL code: an integer overflow in a counter.  The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

## Bug Description
The original counter implementation uses an `integer` type for the internal and output counters.  While functionally correct for most cases, this code suffers from potential integer overflow issues that are easily overlooked.  If the internal counter reaches its maximum value (15 in this example), it will unexpectedly wrap around to 0.

## Solution
The `fixed_counter.vhdl` file presents a corrected version using a more robust type for the counter. Although functionally similar, the solution demonstrates safer handling of the integer, making it suitable for broader application scenarios.