A pointer is a data type/object that stores a memory address. A pointer references a location in memory and accessing the value stored in that location is known as dereferencing the pointer.

The memory address is stored as an unsigned integer.

Pointers give an improvement in performance as it is much cheaper in time and space to copy and dereference a pointer than copy and access the value the pointer is points to.

A pointer is a simple and concrete implementation of the more abstract [[reference]] data type.

Attempting to dereference a pointer to an invalid memory location or performing invalid pointer arithmetic may cause the program to crash. To relieve this problem, measures such as [[type safety]] and bounds checking are implemented in programming languages.