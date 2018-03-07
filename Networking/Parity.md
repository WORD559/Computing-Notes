# Parity #

We can see whether data that has been transmitted by using parity. This only works if there are an odd number of errors in the transmission.

The computers will agree on a parity system (ie. Odd or Even) and will make the number of 1s per byte fit that system. For example, to make 1100101 fit even parity, we prepend a 0 to make 01100101, but for 1011000 we would have to prepend a 1 to make 110110000. If the end computer receives a byte that doesn't fit the system, it will be rejected. Depending on the protocol, this means different things. With telecommunications protocols, rejected data is just discarded. With important things, it will request it be resent.

My name in hex with even parity = 6537f9f46042e17272e1f3f3
