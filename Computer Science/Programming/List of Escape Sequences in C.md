1. **\a :** alert character - produces a beep sound if terminal supports it
2. **\b :** backspace - also works if terminal allows it
3. **\f  :** formfeed - earlier used as a page separator but now used as section separator or page break and looks like this:
	```
	sturgee@sturgee:~/SwapProj$ ./alert
	This is a formfeed character:
	                             sturgee@sturgee:~/SwapProj$
	```
4. **\n :** newline
5. **\r :** carriage return - goes to the beginning of the line
6. **\t :** horizontal tab
7. **\v :** verical tab
8. **\ \ :** backslash - so that the compiler knows that it is used as a string and not as an escape sequence
9. **\ ? :** question mark- so that the compiler knows it is used a a string and not as a ternary operator
10. **\ ' :** single quote - so that the compiler can understand ''' (written as '\'') 
11. **\ " :** double quote - so that the compiler knows it is used as a string and does not close the string it is a part of
12. **\ooo :** octal number - converts octal number to ascii equivalent character (ex. \072 -> ':')
13. **\xhh :** hexadecimal number - converts hexadecimal number to ascii equivalent character (ex. \x4a -> 'J')
14. **\0 :** null character - character with ascii value 0 (literally '')