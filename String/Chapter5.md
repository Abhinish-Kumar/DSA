# Operations on String

## 1. Length of a String.

Length :- Number of characters present in a String. 

### In c find the length of string

- We have to find the `\0` in array of character
- Scan/traverse the array of character until you reach to `\0`

`loop i = ** \0** ==> Stop`

By usign "" , "welcome" - compiler will convert it to array and put `\0` at last of it. 


```c
#include <stdio.h>

int main() {
    char *s = "welcome";
    int i;

    for(i = 0; s[i] != '\0'; i++) {
        // The loop simply increments 'i' to count the characters until it reaches null
    }

    printf("Length is %d\n", i);
    return 0;
}

```

Note:- In javascript 










