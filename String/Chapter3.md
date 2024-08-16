# Importance of ASCII Code and Unicode in Programming

## ASCII Code

### **1. Basic Character Representation**
- **Purpose:** ASCII (American Standard Code for Information Interchange) represents a basic set of characters, including letters, digits, punctuation, and control characters.
- **Range:** Uses 7 bits to encode 128 characters.
- **Use Case:** Essential for early computing systems, simple text files, and protocols.

### in C
```c
char temp;
temp = 'A'; // ✅ Correct
temp = 'AB'; // ❌ Incorrect
temp = A; // ❌ Incorrect
temp = "A"; // ❌ Incorrect


```

Use only Single Quote;
=> A is not stord in temp memory address 65 is stored.

```c
printf("%c", temp); // Output: A (Character)
printf("%d", temp); // Output: 65 (Decimal value of ASCII for 'A')


```


This markdown explanation provides a clear understanding of valid and invalid assignments for the `char` type in C, along with how to correctly print the character and its ASCII value.


Summary 

char temp occupy some memory of 8bytes (1bit) in the memory and represents that location of memory adress with a name called **temp** and in that memory we have 8 bits space what is occupied by ASCII code of A which is `65`.
Note one thing that characters are stored in the memory as their ASCII code. 

1. Printing the Character:
- The `%c` format specifier tells `printf` to interpret the value of `temp` as a charact The %d format specifier tells printf to print the integer value of temp, which corresponds to its ASCII code.er and print it.

2. Printing the ASCII Code:
-  The `%d` format specifier tells `printf` to print the integer value of `temp`, which corresponds to its ASCII code.

```c
#include <stdio.h>

int main() {
    char temp = 'A';  // 'A' is stored as ASCII value 65

    printf("Character: %c\n", temp); // Prints: A
    printf("ASCII Value: %d\n", temp); // Prints: 65

    return 0;
}
```





## Unicode

### **1. Global Character Representation**
- **Purpose:** Unicode provides a comprehensive character set that includes virtually all characters from written languages, symbols, and emojis.
- **Range:** Supports over 1.1 million characters, using code points ranging from `U+0000` to `U+10FFFF`.


**In Summary:**
- **ASCII:** Essential for simple character encoding and legacy systems, providing a foundation for more complex encodings.
- **Unicode:** Critical for modern applications, enabling consistent, global character representation and supporting diverse languages and symbols.



