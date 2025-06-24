single-step-6502
================

This repository contains KiCad sources for a simple single-step controller
module for the 6502 microprocessor. It's designed to be connected to the
system under test using jumpers. It has a pin header that provides +5 VDC,
ground, and the 6502's SYNC and RDY signal paths.

![Single Step Controller Image](single-step-6502.png)

The controller has two push buttons.

1. **Run/Stop** -- is used to toggle between the free running and 
   single-step modes. In the free running mode, the green status LED is 
   illuminated.
2. **Step** -- is used to advance the processor by a single instruction when
   the CPU is stopped. While the CPU is stopped, the red status LED is 
   illuminated.

The buttons are debounced via the 555 and 74123 ICs to avoid triggering
multiple step pulses.

The circuit is designed with a diode such that it can be connected to the 
6502's RDY input without disrupting other uses of the signal.

See [single-step-6502.pdf](single-step-6502.pdf) for a full description
of the circuit design.
