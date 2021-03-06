sha512
======

Verilog implementation of the SHA-512 hash function. This implementation
complies with the functionality in NIST FIPS 180-4. The supports the
SHA-512 variants SHA-512/224, SHA-512/256, SHA-384 and SHA-512.


## Implementation details ##
The core uses a sliding window with 16 64-bit registers for the W
memory. The top level wrapper contains flag control registers for init
and next that automatically resets. This means that the flags must be
set for every block to be processed.


## FPGA-results ##

### Xilinx FPGAs ###
Implementation results using ISE 14.7.

***Artix-7***
- xc7a200t-3fbg484
- 4869 Slice LUTs
- 1575 Slices
- 3918 regs
- 96 MHz


***Spartan-6***
- xc6slx45-3csg324
- 4333 LUTs
- 1300 Slices
- 3853 regs
- 57 MHz


### Altera FPGAs ###

***Altera Cyclone V GX***
- 2923 ALMs
- 3609 Registers
- 80 MHz max clock frequency


## Status ##

***(2016-08-10)***

Added results for Xilinx Artix-7.


***(2014-11-07)***

Added results for Xilinx Spartan-6.


***(2014-04-05)***

RTL for the core and top is completed Testbenches for core and top
completed. All single block and dual block test cases works. Results
after building the complete design for Altera Cyclone V GX:

- 2919 ALMs
- 3609 Registers
- 77 MHz max clock frequency


***(2014-03-24)***

Core works for the SHA-512 mode case. Added top level wrapper and built
the design for Altera Cyclone V GX:

- 2923 ALMs
- 3609 Registers
- 80 MHz max clock frequency



***(2014-02-23)***

Initial version. Based on the SHA-256 core. Nothing really to see yet.
