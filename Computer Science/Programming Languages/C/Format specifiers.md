# Format Specifier

A format specifier is used to describe the data type to the compiler that is to be printed or scanned in input and output operations.
```
number = 231;
printf("This is using a format specifier: %d", number);
```


# Format Specifier types

**%c** :              char (character) data type
**%d** :              int (integer - signed) data type
**%u** :              unsigned int data type - prints positive even when value passed is negative
**%f** :               float (floating point) data type
**%e (or %E)** :  float expressed in exponential form
**%o** :              octal (unsigned) integer number (converts int to octal before printing)
**%x (or %X)** : hexadecimal (unsigned) for integer number (converts int to hex)
**%s** :              string (prints character array for char in array != \0) - only scans up to a whitespace while using `scanf("%s", str)`[^1] and not \0
**%p** :              pointers (address that the pointer is pointing to)

For the following code:
```
#include <stdio.h>

int main(){
    float a = 12.67;
    printf("Using %%e: %e\n", a);
    
    int b = 67;
    printf("%o\n", b);
    
    int c = 15454;
    printf("%X\n", c);
    
    int d = 10;
    printf("The Memory Address of a: %p\n", &d);
    return 0;
}
```

The output will be:
```
Using %e: 1.267000e+01
103
3C5E
The Memory Address of a: 0x7fffccc6cafc
```

[^1]: Modifications can be made to the format specifier as stated in [[Scanset|scansets.]]
