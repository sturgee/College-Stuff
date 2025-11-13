printf(); statement in languages such as Java and C allow a wide range of formatting options.

The general format for a [[Format specifiers|format specifier]] is as follows:
`%[flags][width][.precision]specifier`
where the syntax enclosed within brackets are optional.

## Flags
`+`                          :     prints a plus before numbers if they are positive
`(`                          :     encloses negative numbers in (parentheses)
`,`                          :     groups number with a comma to separate thousands (java only)
`<space>`               :     prints a minus if negative and space if positive

For the code:
```
#include<stdio.h>

int main() {
    int integer = -25;
    printf("The number is % d\n" , integer);
    printf("The number is %+d\n" , integer);
    integer = 1;
    printf("The number is % d\n" , integer);
    return 0;

}
```

The output would be:
```
The number is -25
The number is -25
The number is  1
```  

## Width and .Precision

**%d**     :    print as decimal integer
**%6d**   :    print as decimal integer, at least 6 character wide
**%f**      :    print as floating point
**%6f**    :    print as floating point, at least 6 character wide
**%.2f**   :    print as floating point, 2 characters after decimal point (rounded up)
**%6.2f** :    print as floating point, at least 6 character wide and 2 after decimal point

For the code:
```
#include<stdio.h>

int main() {

    float variable = 5663.2361;

    printf("This is a format of %%3.2f: %3.2f\n", variable);

    return 0;

}
```

The output will be as follows:
```
sturgee@sturgee:~/SwapProj$ ./formatSpecifier
This is a format of %3.2f: 5663.24
```


#Note
##### Note: To print the percentage symbol '%', escape characters are not used like in the case of \ ' and \ ". Instead '\%%' is used.

### Padding (also comes under width)

Used for alignment in a vertical list of numbers. 

For the code:
```
#include<stdio.h>

int main() {

    int num1 = 1544;

    int num2 = 412;

    int num3 = 12;

    int num4 = 3;

    printf("%04d\n%04d\n%04d\n%04d\n" , num1, num2, num3, num4);

    return 0;

}
```

The output would be:
```
1544
0412
0012
0003
```

The above is called zero padding.
The same can be done without zeros by changing the printf() statement to:
`printf("%4d\n%4d\n%4d\n%4d\n" , num1, num2, num3, num4);`

The output would then be:
```
1544
 412
  12
   3
```