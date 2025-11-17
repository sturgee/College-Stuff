Scansets in C are specifiers used to specify the set of characters the  `scanf()` function would read and store inside the character array when called. The characters not within the scope of the scanset are not accepted and `scanf()` stops reading characters when such a character is encountered.

Scansets are defined by placing the range of characters or excluded characters inside `
[]`. Different elements in the scanset may or may not be separated by a `,`. A negated set starts with `^` and every following character or character range is not accepted. A negative set and a positive set cannot be combined.

When a scanset is defined, the syntax `scanf("%[...]", char*)` can be used instead of `scanf("%[...]s", char*)`.

For the code:

```
#include<stdio.h>

int main() {

    char str[64];

    printf("Enter the sentence:\n");

    scanf("%[^A-Za-z,.]", str);

    printf("Str is \"%s\"\n", str);

}
```

The output will be:

```
sturgee@sturgee:~/SwapProj$ ./scanset
Enter the sentence:
67???   LOL!!
Str is "67???   "
```