single-step-6502
================

This repository contains KiCad sources for a simple single-step controller
module for the 6502 microprocessor. It's designed to be connected to the
system under test using jumpers. It has a pin header that provides +5 VDC,
ground, and the 6502's SYNC and RDY signal paths.

![Single Step Controller Image](single-step-6502.png)

The controller has two push buttons.

1. Run/Stop -- is used to toggle between the free running and single-step
   modes. In the free running mode, the green status LED is illuminate
2. Step -- is used to advance the processor by a single instruction. While
   stopped, the red status LED is illuminated.



