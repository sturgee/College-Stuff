The exponent part of the floating point representation allows for a range of exponent values: positive, negative, and 0.

This representation of negative numbers is done without a sign bit because 2's complement representation does not assign values sequentially and comparison of numbers becomes easier.

For n number of bits the values of $-2^{n-1}$  to  $2^{n-1}-1$ can be stored in the exponent part. However these values are stored after adding a bias of $2^{n-1}$.

For example, in a 32 bit representation, the exponent can store true values from -126 and 127. This translates to a range of 1 to 254 (0 and 255 are used for special cases).