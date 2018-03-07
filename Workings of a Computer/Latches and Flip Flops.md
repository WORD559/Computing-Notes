# Latches and Flip Flops #

## SR Latch ##

Set/Reset latch.

When using NOR gates:
  
- Powering set makes Q=1, and then powering reset makes Q=0. This is active high.
- Controlled by pulses; S or R are not left constantly high

When using NAND gates:

- S and R are kept high and controlled by dropping the power. This is active low.

SR latches have invalid states when both S and R are trying to change the state.

SR Latches can be used to counteract "bounce" from mechanical switches.

## Gated SR Latch ##

The gated SR latch allows for enabling or disabling latching. This works by (N)ANDing the inputs at S and R with input E. While E is low, toggling S or R will not change the content of the latch.

## Gated D Latch ##

A Data Latch is a 1-bit memory device.
These are used to counteract the invalid states of SR Latches.

A Gated D uses NOT S as the R input in a Gated SR latch. This makes the invalid states impossible.
It can also be constructed without the use of a NOT gate by taking the top NAND gate and feeding it into the bottom gate.

The output will always match D only when E is enabled.

[Diagram of a Gated D-Latch](D-latch.png)

## Clocked D Latch ##

These D Latches use the input E from a clock, and only respond to changes in D on the rising edge. This is achieved with CC'. Boolean algebra says this should always be 0, but NOT gates are not instantaneous. There is a very brief period where C is high and C' is high, which gives us a minute pulse that can be used as the E input so that it captures data inputs in an "instant".

PRESET and CLEAR inputs can be added, which are asynchronous inputs. CLEAR allows you to bypass the D input and guarantee a 0. PRESET allows you to bypass the D input and guarantee a 1.

Voltage graphs can be used to describe the circuit.
