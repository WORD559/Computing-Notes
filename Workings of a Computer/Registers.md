# Registers #

Registers are a way of storing data close to the CPU so that they can be accessed much faster. They are used for many different things.

- The control unit uses registers to store details of operations being dealt with by the fetch-execute cycle.
- The ALU requires somewhere to put the results of any operations it carries out.
- They have a very limited storage, but play a vital part in the operation of the computer.

## Current Instruction Register ##

Stores the instruction currently being used.

## Program Counter ##

Stores the memory location of the next instruction that will be needed by the processor.

## Memory Buffer Register ##

(Aka Memory Data Register) holds the data that has just been read from or is about to be written to main memory.

## Memory Address Register ##

Stores the memory location where data in the MBR is about to be written or read from.

## Status Register ##

The status register keeps track of the status of various parts of the computer, for example if an overflow error has occurred.

## Interrupt Register ##

This interrupt register is a type of status register. It stores details of any signals that have been received by the processor from other components attached to it, such as the I/O controller for the printer.
