# String (ab)

## Character set / ASCII code 

- Character set are the set of characters that are supported by a programming  language like c, c++ same  as characterSet supported by a computer system.
- Computer system work on a **Binary Number System** , So everything in a computer is a number. They do not support character.
- We define some set of numbers as charcters.
- For Every character we define some numeric value, So we give Some numeric code.
- For english alphabets for every character. There are some codes define those codes are standard codes.
- Every electronic machine follow that same set of code and thode codes are callled as the **American Standard Code for Information Interchange** (ASCII) given by ISO Standard.
- And for other languages we have UNICODEs

#### ASCII code for English language.

```c
//26 upper case

A -- 65 
B -- 66
-
-
Z -- 90


//26 lowercases

a -- 97
b -- 98
-
-
z -- 122


//0 -- 9

0 -- 48
1 -- 49
-
-
9 -- 57

```
All are symbols

Every Symbol in the keyboard defines a character set and for every keyboard there is same ASCII code available. 



Note :- we have total 128 ASCII codes

7 bits are sufficient =  ** 2^7 = 128  **

from **0---- 127**


All the ASCII characters

<img src="https://learnlearn.uk/binary/wp-content/uploads/sites/11/2017/01/ASCII-Table-wide.svg_.png" width="100%" background="white" />

1. Enter --- 10
2. Space Bar --- 13
3. Escape --- 27

Summary 

1. ASCII stands for ** American Standard Code for Information Interchange**
2. It is the most common format for files of computer
3. It maps Binary To letters / Numbers
4. It represents text which maked it possible to transfer from one computer to another , It act as a common languge code for computers to communicate.
5. The ASCII is a **7bits** code whose format is X^6 X^5 X^4 X^3 X^2 X^1 X^0, where each X is o or 1.
6. It represents English Language Characters (letters, numbers , symbols and punctuations).

# extended ASCII / 8bit ASCII


## Differences Between 7-bit ASCII and 8-bit ASCII

### 7-bit ASCII

- **Character Set**: Uses 7 bits for each character, allowing for **128 different characters** (`2^7 = 128`).
- **Range**: Character codes range from **0 to 127**.
- **Content**: Includes basic English letters (both uppercase and lowercase), digits, punctuation marks, and a few control characters (such as newline and carriage return).
- **Standard**: 7-bit ASCII is the original ASCII standard.

### 8-bit ASCII

- **Character Set**: Uses 8 bits for each character, allowing for **256 different characters** (`2^8 = 256`).
- **Range**: Character codes range from **0 to 255**.
- **Content**: Includes all 128 characters of 7-bit ASCII plus additional characters such as special symbols, accented letters, and other characters useful in various languages and applications.
- **Extension**: Often referred to as **extended ASCII**. Various extended ASCII sets exist, such as ISO 8859-1 (Latin-1), which includes characters for Western European languages.

### Summary

While 7-bit ASCII provides a basic set of characters suitable for English and control functions, 8-bit ASCII offers a broader range of characters to support additional languages and symbols.








