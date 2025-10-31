The Gray Code (also known as Reflected Binary Code) is an ordering of binary number system such that two successive values differ in only one bit.
Gray codes are used to prevent invalid output from electromechanical switches and facilitate error correction in digital communications.

#### Conversion Table of Gray Code:

| Decimal | [[Code Translation#^723bf7\|Binary]] | Gray |
| :-----: | :----------------------------------: | :--: |
|    0    |                 0000                 | 0000 |
|    1    |                 0001                 | 0001 |
|    2    |                 0010                 | 0011 |
|    3    |                 0011                 | 0010 |
|    4    |                 0100                 | 0110 |
|    5    |                 0101                 | 0111 |
|    6    |                 0110                 | 0101 |
|    7    |                 0111                 | 0100 |
|    8    |                 1000                 | 1100 |
|    9    |                 1001                 | 1101 |
|   10    |                 1010                 | 1111 |
|   11    |                 1011                 | 1110 |
|   12    |                 1100                 | 1010 |
|   13    |                 1101                 | 1011 |
|   14    |                 1110                 | 1001 |
|   15    |                 1111                 | 1000 |

### Conversion mechanism of Binary to Gray:

1. Most significant bit stays the same.
2. Consecutive Gray Code bits at index i is determined by (Binary[i-1])XOR(Binary[i]) i.e. the exclusive or of the Binary bit at same index and it's previous index.

$$G(i) = i \textasciicircum (i >> 1)$$
where i is the binary number, ^ is the bitwise XOR operator, and >> is the bitwise right shift operator.

**Example:** 
1. Binary: 100110
	1  ^ 0 ^  0 ^ 1 ^ 1 ^  0           Binary
	|       |      |      |      |      |
	1     1     0     1     0     1           Gray

2. Binary: 1011
	1  ^ 0 ^  1 ^ 1                        Binary
	|       |      |      |
	1     1     1     0                        Gray

### Conversion mechanism of Gray to Binary:

1. Most significant bit stays the same.
2. Consecutive Binary bits at index i is determined by (Binary[i-1])XOR(Gray[i]) i.e. the exclusive or of the current Gray Code bit and the previous Binary bit.

**Example:**
1. Gray: 110101
    1      1      0     1     0     1           Gray
	|   /   |   /  |  /   |  /  |  /   |
	1      0     0     1     1     0           Binary

2. Gray: 0100
	0      1      0     0                         Gray
	|   /   |   /  |  /   |
	0      1     1     1                         Binary