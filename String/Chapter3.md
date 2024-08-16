# Importance of ASCII Code and Unicode in Programming

## ASCII Code

### **1. Basic Character Representation**
- **Purpose:** ASCII (American Standard Code for Information Interchange) represents a basic set of characters, including letters, digits, punctuation, and control characters.
- **Range:** Uses 7 bits to encode 128 characters.
- **Use Case:** Essential for early computing systems, simple text files, and protocols.

## Unicode

### **1. Global Character Representation**
- **Purpose:** Unicode provides a comprehensive character set that includes virtually all characters from written languages, symbols, and emojis.
- **Range:** Supports over 1.1 million characters, using code points ranging from `U+0000` to `U+10FFFF`.


## in C
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


## In javascript
In JavaScript, characters are handled differently compared to languages like C, especially with respect to encoding and memory representation. Here’s an overview of how JavaScript manages characters and their ASCII (or Unicode) codes:

### 1.  String Representation

1. String Type:- In JavaScript, characters are represented as strings. A JavaScript `string` can contain zero or more characters.
2. Single Characters:- JavaScript does not have a separate `char` type like C. Instead, strings are used to represent characters.

```javascript

let temp = 'A';  // 'A' is a string containing a single character

```

### 2.  Character Encoding

"JavaScript strings are encoded in UTF-16"


#### UTF-16 Encoding

1. What is UTF-16?

UTF-16 is a way to encode `characters` as a sequence of `16-bit` code units. Think of it as a system for storing characters in a computer using `16-bit` "chunks" or units.

UTF-16 Example: 
# Character Representation in Different Encodings


# UTF-16 Encoding Example

| **Character** | **16-bit Binary** | **Memory Storage** |
|---------------|-------------------|--------------------|
| 'A' (65)      | `00000000 01000001` | `0x0041`          |


2. How does it works?

- Basic Characters: For most common characters (like those in the ASCII set), UTF-16 uses a single 16-bit unit. For example, the character `'A'` is stored as a 16-bit unit with the value `0x0041` (65 in decimal).
- Extended Characters: For characters beyond the basic set, such as some emoji or special symbols, UTF-16 uses two 16-bit units. This is known as a `"surrogate pair."`


### Example
1. Single 16-bit Unit:

```javascript

let char = 'A';
console.log(char.charCodeAt(0)); // Output: 65

```

Here, `'A'` is encoded with a single 16-bit unit, `0x0041`.


2. Surrogate Pair:

```javascript

let emoji = '😀';
console.log(emoji.charCodeAt(0)); // Output: 55357
console.log(emoji.charCodeAt(1)); // Output: 56834

```
The emoji `'😀'` is encoded with two 16-bit units. The code units are `0xD83D` and `0xDE00`, which together represent the full Unicode code point for this emoji.


## Unicode Code Points

### What are Unicode Code Points?
Unicode Code Points are unique numbers assigned to every character in the Unicode standard. These numbers represent characters from various writing systems, symbols, and emoji.

### How Does JavaScript Use Them?
- Basic Character Code Point:

```javascript

let char = 'A';
console.log(char.codePointAt(0)); // Output: 65

```
The Unicode code point for `'A'` is `65`.

- Extended Character Code Point:

```javascritp
let emoji = '😀';
console.log(emoji.codePointAt(0)); // Output: 128512

```
The Unicode code point for `'😀'` is `128512`, which is beyond the range of a single 16-bit unit, hence it uses a surrogate pair in UTF-16.

- UTF-16 Encoding: JavaScript strings use UTF-16, which means each character is stored as either one or two 16-bit units. Most common characters are stored in one unit, while more complex characters use two units (a surrogate pair).
- Unicode Code Points: Every character has a unique Unicode code point. JavaScript can handle these code points and convert them into the UTF-16 encoding used internally.





