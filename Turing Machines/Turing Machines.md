# Turing Machines #

The Turing Machine was a thought experiment proposed by Alan Turing. It was a theoretical machine proposed to solve "The Decision Problem".

The machine is able to read from and write to individual "cells" on an infinitely long tape, and make decisions based on the contents of the tape. The machine has an alphabet, for example "0", "1", and "". 

## State Transition Diagrams ##

These behave very much the same as finite state machines.

`Insert paper diagrams`

## Instruction Tables ##

We can represent all of the possible states and movements around the machine.

|Start State|Read|Write|Move|End State|
|:---------:|:--:|:---:|:--:|:-------:|
|S0         |0   |0    |R   |S0       |
|S0         |1   |1    |R   |S1       |
|S0         |    |1    |R   |SH       |
|S1         |0   |0    |R   |S1       |
|S1         |1   |1    |R   |S0       |
|S1         |    |0    |R   |SH       |

## Transition Rules ##

These are effectively the same as the same, but they are written in the following form:

`δ(start state,read)=(end state,write,move)`

So `δ(S0,0)=(S0,0,R)` is the same as the first row of the table above.

