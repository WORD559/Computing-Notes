# Architectures #

## Von Neumann Architecture ##

- Data and instructions are kept in the same memory and travel along the same bus.

## Harvard Architecture ##

- Data and instructions have separate memory, address different parts of memory, and travel along separate buses.
- This means that 4 buses are required; the data bus, the instruction bus, and address buses for both.
- This can often be more expensive to implement, but in specialised systems it is important.
    - Integrated systems often use Harvard architecture.
    - Critical systems where speed is of the essence (such as remote surgery) also use this.
