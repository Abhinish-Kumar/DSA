# String 

`Array of characters`

## What is a String in C?
- In C, a string is essentially an array of characters terminated by a null character (`'\0'`). This null character indicates the end of the string.

- `\0` at the end of the array , of character makes it string , without it we can not say that its a string.

- Without it, functions that operate on strings will not know where the string ends, which can lead to undefined behavior.
- Here’s a demonstration to prove why the null character is essential for treating an array of characters as a string:

```c

#include <stdio.h>
#include <string.h>

int main() {
    // Array without null terminator
    char arr1[5] = {'H', 'e', 'l', 'l', 'o'};
    
    // Array with null terminator
    char arr2[6] = {'H', 'e', 'l', 'l', 'o', '\0'};

    // Print the arrays as strings
    printf("Array without null terminator (attempt to print):\n");
    printf("%s\n", arr1); // Undefined behavior, might print garbage

    printf("Array with null terminator:\n");
    printf("%s\n", arr2); // Correctly prints "Hello"

    // Demonstrate strlen behavior
    printf("Length of array without null terminator: %lu\n", strlen(arr1)); // Undefined behavior
    printf("Length of array with null terminator: %lu\n", strlen(arr2)); // Prints: 5

    return 0;
}

```

`\0` this is also called as 
1. String delimeter
2. End of string character
3. null character
4. String terminator

We can not find length of a string without null character in c and c++.

To make it string in c we have to pass a null at the end of the character of the array. Without this, this is just  a array of characer not a string.

Note:- In JavaScript, strings are always treated as sequences of characters enclosed in quotes (`' '`, `" "`, or ` `). Unlike C, JavaScript strings do not require a null terminator to signify the end of the string. The JavaScript runtime handles strings internally with built-in methods that manage their length and content. Therefore, JavaScript strings inherently include their length information and do not need a special character to indicate their end.


## Methods to Declare String.

## 1. Character Array with Individual Assignment
```c

char str5[6] = {'H', 'e', 'l', 'l', 'o', '\0'}; // Explicit null terminator

char helloString[] = {'H', 'e', 'l', 'l', 'o', '\0'};

```

Each character is assigned individually, and the null terminator must be explicitly included to mark the end of the string.

## 2. Character Array Initialization

1. Implicit Size Initialization

```c

char str1[] = "Hello, World!"; // Array size is automatically determined

```

The compiler calculates the size of the array to fit the string and the null terminator (`'\0'`).

2. Explicit Size Initialization

```c

char str2[20] = "Hello, World!"; // Array size is 20, string fits within it

```
If the string is shorter than the array size, the rest of the array elements are initialized to '`\0`'

- **If we use double Quotes compiler automatically add `\0` to it.**

## 3. String Literals (Created in heap)/ Character Pointer

```c

char *str6 = "Hello, World!"; // Pointer to a string literal

```
This declares a pointer to a string literal stored in read-only memory. Modifying the string literal directly is undefined behavior.


Note:- You can declare and initialize strings in various ways in `javascript`


## 1. String Literals

You can declare and initialize a string directly using single quotes `(' ')`, double quotes `(" ")`, or backticks `(` `)`:

```javascript

let str1 = 'Hello, World!'; // Single quotes
let str2 = "Hello, World!"; // Double quotes
let str3 = `Hello, World!`; // Template literals (backticks)

```
Backticks (`` ``): Used for template literals, allowing embedded expressions and multiline strings.

## 2. Multiline Strings
Using backticks, you can create multiline strings:

```javascript

let multilineStr = `This is a string
that spans multiple
lines.`;

```

Backticks allow for the inclusion of line breaks and more readable multiline strings.

## 3. String Object Constructor

```javascript

let str5 = new String('Hello, World!');

```
- The `String` constructor creates a String Object
- Which is different from a primitive from a primitive string
-  It includes additonal methods, but primitive strings are good , or preferred.















