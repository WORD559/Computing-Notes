# Stored Program Concept #

- How instructions are handled using the stored program concept
- What happens at each stage of the fetch-execute cycle
- That a processor is made up of components including registers and units
- How the registers and units are used to handle instructions
- What factors affect processor performance
- What an interrupt is and how a processor handles it
- The von Neumann concept is to store instructions and data in the same memory unit.
- It was designed so that general purpose computers could be designed and the instructions kept in memory with the data, instead of the actual computer being the program and having to rebuild the computer to change the program.
- Each instruction or data item is fetched from memory, decoded, and then executed, with any new data created being placed back into memory.
- Every time a program is run, the processor runs through the fetch execute cycle.

## Fetch-Execute Cycle ##

1. Fetch the instruction from memory
2. Decode the fetched instruction to determine what to do
3. Execute the instruction. This can be reading data from memory into the accumulator, performing a calculation on the data, writing the data back to memory, etc.

This is controlled by the control unit. The control unit is also responsible for making sure that all the data that is being processed is routed correctly. Data is put into the correct register or section of memory by the control unit.