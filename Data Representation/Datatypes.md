# Data types #

Be Careful
Bears Shouldn't Ingest Large
Furry Dogs

## Primitive Datatypes ##

B oolean - 1 bit (sort of)

C har - 7 bits (for ASCII) or 16/32 bits (for Unicode)

B yte - 8 bits
S hort - 16 bits
I nt - 32 bits
L ong - 64 bits

F loat - 32 bits
D ouble - 64 bits

## Composite Datatypes ##

List
Array
String



# Stack vs Queue #

Stacks are LIFO (Last In First Out)
Queues are FIFO (First In First Out)

## Queues ##

The first item put in is the first item to be dealt with.

There is also priority queuing - the first items are typically the first to be dealt with, but more important items are dealt with first.

"Enqueueing" is the process of adding something to the back of a queue. "Dequeueing" is the process of removing the item at the front of the queue.

### Implementation ###

You can implement the queue as a list with a pointer to the front of the queue and a pointer to the back of the queue. When the two pointers have the same value, the queue is empty. When a value is added, the back of the queue is incremented by one, and when a value is removed the front of the queue is decreased by one. The pointers will loop around in modular arithmetic (like a clock) to fill spaces from dequeueing. In this instance, known as circular queueing, if the front of the queue = back back of queue + 1, the queue is empty.

A priority queue is slightly more complex to implement. You must iterate through the list from the front of the queue for each level of priority. The queue must then be reorganised to maintain its structure.

## Stacks ##

With a stack, the last thing pushed onto the stack is the first thing to be popped off the stack.

### Implementation ###

A stack can be implemented as a pointer to the last item in a list. As new items are pushed onto the stack, the pointer's value increases, and as items are popped off of the top, the pointer's value decreases.

