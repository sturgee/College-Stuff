To store a decimal number in binary the decimal number is first converted to binary. This binary number is then expressed in exponential form similar to scientific notation.

For example, the number $5.125$ is $(101.001)_2$ and will be represented as $1.01001*2^2$ (as per [[Explicit and Implicit Normalization#Implicit Normalization| Implicit Normalization]]).

A 32 bit float variable can be broken up into 3 parts:
1. Sign bit (1 bit)
2. Exponent (8 bits)
3. Mantissa (23 bits)

## 1. Sign Bit
This is the MSB (Most Significant Bit) and stores the sign of the entire number. This will be 0 in the case of $5.125$ as it is positive.

## 2. Exponent
This part stores the exponent part of the implicit normalization of the number after [[Bias |biasing.]] In this case, the exponent is 2 as the radix point shifted two places to the left. Thus after adding a bias of 127 (for exponent part with 8 bits), it becomes 129 and is stored as 10000001.

The exponent part can store between 0 and 255 but 0 and 255 are reserved for special cases.

## 3. Mantissa
The bits after the decimal point are stored in this part and called the mantissa. In this case, it will be 01001. More specifically, it will be 01001 followed by 0s until all bits are "extinguished."

The formula $(-1)^S \: 1.M \: 2^{E \: - \: Bias}$ can be used where S is the sign, M is the mantissa and E is the exponent.

The formula will be  $(-1)^S \: 0.M \: 2^{E \: - \: Bias}$ if explicit normalization is used.

# Special representation

- Zero is represented as both exponent and mantissa as zero.
- + and - infinity are represented as all 1 exponent and 0 mantissa.
- Not a number (NaN) is represented as all 1 exponent and non-zero mantissa