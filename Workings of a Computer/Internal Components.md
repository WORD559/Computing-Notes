# Internal Components #

- A computer is ANY device that processes data.
- The word computer also implies that it is an electronic or digital device.
- In simple terms this means that it will contain one or more microprocessors that can be programmed to control the device.
- Microprocessors are made up of microscopic electronic circuits and belong to a group of devices commonly referred to as chips.
- Custom chips canbe produced! It's normally just a silicon board with transistors on it, so custom chips can be developed to make the chip work the way it should.

## CPU ##

- The processor is a device that carries out computation on data by following instructions.
- It handles all of the instructions that it receives from the user and from the hardware and software.
- Physically, the processor is made up of a thin slice of silicon approximately 2cm 2
- Using microscopic manufacturing techniques, the silicon is implanted with millions of transistors.
- The computer's clock speed is measured in (G)Hz. 
- IN THE SAME SETUP, a faster CPU results in a faster computer.

## Moore's Law ##

- This is the idea that the number of transistors you can fit per square inch will double every year.
- Moore's law has slowed down a bit (to doubling about once every 18 months) but is still fairly accurate.
- Biocomputing could potentially be used to beat Moore's law.

## Buses ##

- Essentially a microscopic wire.
- Connect transistors, I/O devices (or their controllers, at least), and components such as registers.
- The transistors are used to control the flow of electrical pulses that are timed via the computer's clock.
- The pulses of electricity represent different parts of the instruction that the processor is carrying out.
- The data bus is bidirectional. It passes information between the memory and the processor. It also connects to the I/O controllers.
- The data bus has to be big enough to send a word to the processor. Therefore in 32-bit, it is 32-bit. In 64-bit, it is 64-bit.
- The address bus is unidirectional, from processor to memory. It is used by the processor to get the specific address in memory. Like all the other buses, it has to match the architecture. This is why 32-bit CPUs can only address 4GB of memory -because the address bus is not big enough to address more than that.
- The control bus is required for synchronisation. It is required to prevent clashes between components and data.

## Memory ##

- Memory is used to store data and instructions. The memory cells will have a width the same as the data bus, which is the length of a word for the processor.
- It is connected to the processor, which will fetch the data andinstructions it needs (you need data to actually do stuff to) from memory, decode the instructions, and then execute them.
- Random Access Memory (RAM) is also known as the Immediate Access Store (IAS) or primary storage.
- It is temporary storage that can be accessed very quickly.
- It is connected directly to the CPU to minimise the access times.
- More is better, because it allows you to store more data and instructions closer to the CPU.
- RAM is volatile! As soon as it loses power, you lose all the data (except for special circumstances like NVRAM)
- Things are normally addressed in memory -this makes it easy for the processor to find what it needs (ie, data, programs, OS, etc.)

## ROM (Read Only Memory) ##

- ROM is a method of storing data and instructions that can be accessed by the computer, typically the BIOS.
- It is not volatile and it is difficultto write to. The contents are not easily lost.

## I/O Controllers ##

- There are dedicated controllers for each port on the computer. They are connected to the CPU via the data bus.
- They translate data from the I/O device into data that can be used by the CPU.
- They also buffer data so that the CPU does not have to wait. Data is then fed to the CPU when it is available.

## Control Unit ##

See "The Stored Program Concept"

## Arithmetic Logic Unit (ALU) ##

- The ALU is responsible for two types of operations; arithmetic and logic (wow, mind blown).
- The ALU can be used to carry out the normal mathematical functions such as add, subtract, multiply and divide, and some otherfunctions such as shifting.
- The ALU is also used to compare two values and decide if one is less than, greater than, or the same as another.
- The ALU is sent an operation code (op-code) and the operands (the data to be processed).
- In some computers, there is a separate ALU for floating point operations. This is because of the complexity of the operations.

## The Clock ##

- All computers have an internal clock.
- The clock generates a signal that is used to synchronise the operation of the processor and the movement of data around the other components of the computer.
- The speed of a clock is measured in either megahertz (MHz) or gigahertz (GHz)
- In 1990, a clock speed of between 4 and 5 MHz was normal.
- In 2000, 1 GHz clock speeds were common.
- Now, the typical clock speed is around 2-3 GHz.

## Cache ##

- Instructions that are needed frequently are placed into a temporary area of memory that is separate from main memory.
- It is closer to the CPU and faster to read from.
- Using cache helps to prevent the CPU from being idle.

## Multiple Cores ##

- One core is one processor. By using multiple cores, you can process multiple things at the same time.

## Factors Affecting Processor Performance ##

### Clock Speed ###

Clock speed is one measure of the performance of the computer.

### Bus Width ###

Increasing the width of the data bus means that more bits, and therefore more data, can be transmitted at any time. It also increases the amount of RAM that can be addressed, which will increase performance.

### Word Length ###

The longer the words, the more data can be manipulated at a time, and the more potential instructions there are. 
