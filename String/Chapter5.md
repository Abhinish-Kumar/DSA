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

```javascript

let s = "welcome";
let i;

for (i = 0; s[i] !== undefined; i++) {
    // The loop increments 'i' to count the characters
}

console.log("Length is " + i);

//O(n) Time Complexity

```

With built-in length property in js.

```javascript

let s = "welcome";
console.log("Length is " + s.length);

```

JavaScript engines maintain the length of the string internally, so retrieving it does not require iterating through the string.
Thus, the time complexity of using the length property is` O(1).`


## Properties of a string in javascript.
In JavaScript, strings are primitive data types and immutable.
1. Length Property:- The `length` property returns the number of characters in a string.

```javascript

let str = "hello";
console.log(str.length); // Output: 5

```

2. Immutability:- Strings in JavaScript are immutable, meaning once a string is created, it cannot be changed. Any operation that appears to modify a string actually creates a new string.

```javascript

let str = "hello";
str[0] = "H"; // This will not change the string
console.log(str); // Output: "hello"

```

3. String Indexing:- Strings are zero-indexed arrays of characters, meaning you can access individual characters using bracket notation.

```javascript

let str = "hello";
console.log(str[0]); // Output: "h"

```
4. Escape Sequences:- Strings can contain special characters using escape sequences (e.g., `\n` for a new line, `\'` for a single quote, `\"` for a double quote).

```javascript

let str = "He said, \"Hello!\"";
console.log(str); // Output: He said, "Hello!"

```
5. Unicode and UTF-16 Encoding:- JavaScript strings are encoded in UTF-16, which means each character is represented by one or more 16-bit code units.

```javascript

let smiley = "😊";
console.log(smiley.length); // Output: 2 (since it's encoded as two 16-bit code units)

```













