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

# 7-bit ASCII Table

| Binary Code | Character | Number |
|-------------|-----------|--------|
| `0000000`   | NUL       | 0      |
| `0000001`   | SOH       | 1      |
| `0000010`   | STX       | 2      |
| `0000011`   | ETX       | 3      |
| `0000100`   | EOT       | 4      |
| `0000101`   | ENQ       | 5      |
| `0000110`   | ACK       | 6      |
| `0000111`   | BEL       | 7      |
| `0001000`   | BS        | 8      |
| `0001001`   | HT        | 9      |
| `0001010`   | LF        | 10     |
| `0001011`   | VT        | 11     |
| `0001100`   | FF        | 12     |
| `0001101`   | CR        | 13     |
| `0001110`   | SO        | 14     |
| `0001111`   | SI        | 15     |
| `0010000`   | DLE       | 16     |
| `0010001`   | DC1       | 17     |
| `0010010`   | DC2       | 18     |
| `0010011`   | DC3       | 19     |
| `0010100`   | DC4       | 20     |
| `0010101`   | NAK       | 21     |
| `0010110`   | SYN       | 22     |
| `0010111`   | ETB       | 23     |
| `0011000`   | CAN       | 24     |
| `0011001`   | EM        | 25     |
| `0011010`   | SUB       | 26     |
| `0011011`   | ESC       | 27     |
| `0011100`   | FS        | 28     |
| `0011101`   | GS        | 29     |
| `0011110`   | RS        | 30     |
| `0011111`   | US        | 31     |
| `0100000`   | Space     | 32     |
| `0100001`   | !         | 33     |
| `0100010`   | "         | 34     |
| `0100011`   | #         | 35     |
| `0100100`   | $         | 36     |
| `0100101`   | %         | 37     |
| `0100110`   | &         | 38     |
| `0100111`   | '         | 39     |
| `0101000`   | (         | 40     |
| `0101001`   | )         | 41     |
| `0101010`   | *         | 42     |
| `0101011`   | +         | 43     |
| `0101100`   | ,         | 44     |
| `0101101`   | -         | 45     |
| `0101110`   | .         | 46     |
| `0101111`   | /         | 47     |
| `0110000`   | 0         | 48     |
| `0110001`   | 1         | 49     |
| `0110010`   | 2         | 50     |
| `0110011`   | 3         | 51     |
| `0110100`   | 4         | 52     |
| `0110101`   | 5         | 53     |
| `0110110`   | 6         | 54     |
| `0110111`   | 7         | 55     |
| `0111000`   | 8         | 56     |
| `0111001`   | 9         | 57     |
| `0111010`   | :         | 58     |
| `0111011`   | ;         | 59     |
| `0111100`   | <         | 60     |
| `0111101`   | =         | 61     |
| `0111110`   | >         | 62     |
| `0111111`   | ?         | 63     |
| `1000000`   | @         | 64     |
| `1000001`   | A         | 65     |
| `1000010`   | B         | 66     |
| `1000011`   | C         | 67     |
| `1000100`   | D         | 68     |
| `1000101`   | E         | 69     |
| `1000110`   | F         | 70     |
| `1000111`   | G         | 71     |
| `1001000`   | H         | 72     |
| `1001001`   | I         | 73     |
| `1001010`   | J         | 74     |
| `1001011`   | K         | 75     |
| `1001100`   | L         | 76     |
| `1001101`   | M         | 77     |
| `1001110`   | N         | 78     |
| `1001111`   | O         | 79     |
| `1010000`   | P         | 80     |
| `1010001`   | Q         | 81     |
| `1010010`   | R         | 82     |
| `1010011`   | S         | 83     |
| `1010100`   | T         | 84     |
| `1010101`   | U         | 85     |
| `1010110`   | V         | 86     |
| `1010111`   | W         | 87     |
| `1011000`   | X         | 88     |
| `1011001`   | Y         | 89     |
| `1011010`   | Z         | 90     |
| `1011011`   | [         | 91     |
| `1011100`   | \         | 92     |
| `1011101`   | ]         | 93     |
| `1011110`   | ^         | 94     |
| `1011111`   | _         | 95     |
| `1100000`   | `         | 96     |
| `1100001`   | a         | 97     |
| `1100010`   | b         | 98     |
| `1100011`   | c         | 99     |
| `1100100`   | d         | 100    |
| `1100101`   | e         | 101    |
| `1100110`   | f         | 102    |
| `1100111`   | g         | 103    |
| `1101000`   | h         | 104    |
| `1101001`   | i         | 105    |
| `1101010`   | j         | 106    |
| `1101011`   | k         | 107    |
| `1101100`   | l         | 108    |
| `1101101`   | m         | 109    |
| `1101110`   | n         | 110    |
| `1101111`   | o         | 111    |
| `1110000`   | p         | 112    |
| `1110001`   | q         | 113    |
| `1110010`   | r         | 114    |
| `1110011`   | s         | 115    |
| `1110100`   | t         | 116    |
| `1110101`   | u         | 117    |
| `1110110`   | v         | 118    |
| `1110111`   | w         | 119    |
| `1111000`   | x         | 120    |
| `1111001`   | y         | 121    |
| `1111010`   | z         | 122    |
| `1111011`   | {         | 123    |
| `1111100`   | \|        | 124    |
| `1111101`   | }         | 125    |
| `1111110`   | ~         | 126    |
| `1111111`   | DEL       | 127    |


### 8-bit ASCII

- **Character Set**: Uses 8 bits for each character, allowing for **256 different characters** (`2^8 = 256`).
- **Range**: Character codes range from **0 to 255**.
- **Content**: Includes all 128 characters of 7-bit ASCII plus additional characters such as special symbols, accented letters, and other characters useful in various languages and applications.
- **Extension**: Often referred to as **extended ASCII**. Various extended ASCII sets exist, such as ISO 8859-1 (Latin-1), which includes characters for Western European languages.

| Binary   | Character | Decimal |
|----------|-----------|---------|
| 00000000 | NUL       | 0       |
| 00000001 | SOH       | 1       |
| 00000010 | STX       | 2       |
| 00000011 | ETX       | 3       |
| 00000100 | EOT       | 4       |
| 00000101 | ENQ       | 5       |
| 00000110 | ACK       | 6       |
| 00000111 | BEL       | 7       |
| 00001000 | BS        | 8       |
| 00001001 | HT        | 9       |
| 00001010 | LF        | 10      |
| 00001011 | VT        | 11      |
| 00001100 | FF        | 12      |
| 00001101 | CR        | 13      |
| 00001110 | SO        | 14      |
| 00001111 | SI        | 15      |
| 00010000 | DLE       | 16      |
| 00010001 | DC1       | 17      |
| 00010010 | DC2       | 18      |
| 00010011 | DC3       | 19      |
| 00010100 | DC4       | 20      |
| 00010101 | NAK       | 21      |
| 00010110 | SYN       | 22      |
| 00010111 | ETB       | 23      |
| 00011000 | CAN       | 24      |
| 00011001 | EM        | 25      |
| 00011010 | SUB       | 26      |
| 00011011 | ESC       | 27      |
| 00011100 | FS        | 28      |
| 00011101 | GS        | 29      |
| 00011110 | RS        | 30      |
| 00011111 | US        | 31      |
| 00100000 | SPACE     | 32      |
| 00100001 | !         | 33      |
| 00100010 | "         | 34      |
| 00100011 | #         | 35      |
| 00100100 | $         | 36      |
| 00100101 | %         | 37      |
| 00100110 | &         | 38      |
| 00100111 | '         | 39      |
| 00101000 | (         | 40      |
| 00101001 | )         | 41      |
| 00101010 | *         | 42      |
| 00101011 | +         | 43      |
| 00101100 | ,         | 44      |
| 00101101 | -         | 45      |
| 00101110 | .         | 46      |
| 00101111 | /         | 47      |
| 00110000 | 0         | 48      |
| 00110001 | 1         | 49      |
| 00110010 | 2         | 50      |
| 00110011 | 3         | 51      |
| 00110100 | 4         | 52      |
| 00110101 | 5         | 53      |
| 00110110 | 6         | 54      |
| 00110111 | 7         | 55      |
| 00111000 | 8         | 56      |
| 00111001 | 9         | 57      |
| 00111010 | :         | 58      |
| 00111011 | ;         | 59      |
| 00111100 | <         | 60      |
| 00111101 | =         | 61      |
| 00111110 | >         | 62      |
| 00111111 | ?         | 63      |
| 01000000 | @         | 64      |
| 01000001 | A         | 65      |
| 01000010 | B         | 66      |
| 01000011 | C         | 67      |
| 01000100 | D         | 68      |
| 01000101 | E         | 69      |
| 01000110 | F         | 70      |
| 01000111 | G         | 71      |
| 01001000 | H         | 72      |
| 01001001 | I         | 73      |
| 01001010 | J         | 74      |
| 01001011 | K         | 75      |
| 01001100 | L         | 76      |
| 01001101 | M         | 77      |
| 01001110 | N         | 78      |
| 01001111 | O         | 79      |
| 01010000 | P         | 80      |
| 01010001 | Q         | 81      |
| 01010010 | R         | 82      |
| 01010011 | S         | 83      |
| 01010100 | T         | 84      |
| 01010101 | U         | 85      |
| 01010110 | V         | 86      |
| 01010111 | W         | 87      |
| 01011000 | X         | 88      |
| 01011001 | Y         | 89      |
| 01011010 | Z         | 90      |
| 01011011 | [         | 91      |
| 01011100 | \         | 92      |
| 01011101 | ]         | 93      |
| 01011110 | ^         | 94      |
| 01011111 | _         | 95      |
| 01100000 | `         | 96      |
| 01100001 | a         | 97      |
| 01100010 | b         | 98      |
| 01100011 | c         | 99      |
| 01100100 | d         | 100     |
| 01100101 | e         | 101     |
| 01100110 | f         | 102     |
| 01100111 | g         | 103     |
| 01101000 | h         | 104     |
| 01101001 | i         | 105     |
| 01101010 | j         | 106     |
| 01101011 | k         | 107     |
| 01101100 | l         | 108     |
| 01101101 | m         | 109     |
| 01101110 | n         | 110     |
| 01101111 | o         | 111     |
| 01110000 | p         | 112     |
| 01110001 | q         | 113     |
| 01110010 | r         | 114     |
| 01110011 | s         | 115     |
| 01110100 | t         | 116     |
| 01110101 | u         | 117     |
| 01110110 | v         | 118     |
| 01110111 | w         | 119     |
| 01111000 | x         | 120     |
| 01111001 | y         | 121     |
| 01111010 | z         | 122     |
| 01111011 | {         | 123     |
| 01111100 | \|        | 124     |
| 01111101 | }         | 125     |
| 01111110 | ~         | 126     |
| 01111111 | DEL       | 127     |

| Binary   | Character | Decimal |
|----------|-----------|---------|
| 10000000 | Ç         | 128     |
| 10000001 | ü         | 129     |
| 10000010 | é         | 130     |
| 10000011 | â         | 131     |
| 10000100 | ä         | 132     |
| 10000101 | à         | 133     |
| 10000110 | å         | 134     |
| 10000111 | ç         | 135     |
| 10001000 | ê         | 136     |
| 10001001 | ë         | 137     |
| 10001010 | è         | 138     |
| 10001011 | ï         | 139     |
| 10001100 | î         | 140     |
| 10001101 | ì         | 141     |
| 10001110 | Ä         | 142     |
| 10001111 | Å         | 143     |
| 10010000 | É         | 144     |
| 10010001 | æ         | 145     |
| 10010010 | Æ         | 146     |
| 10010011 | ô         | 147     |
| 10010100 | ö         | 148     |
| 10010101 | ò         | 149     |
| 10010110 | û         | 150     |
| 10010111 | ù         | 151     |
| 10011000 | ÿ         | 152     |
| 10011001 | Ö         | 153     |
| 10011010 | Ü         | 154     |
| 10011011 | ø         | 155     |
| 10011100 | £         | 156     |
| 10011101 | Ø         | 157     |
| 10011110 | ×         | 158     |
| 10011111 | ƒ         | 159     |
| 10100000 | á         | 160     |
| 10100001 | í         | 161     |
| 10100010 | ó         | 162     |
| 10100011 | ú         | 163     |
| 10100100 | ñ         | 164     |
| 10100101 | Ñ         | 165     |
| 10100110 | ª         | 166     |
| 10100111 | º         | 167     |
| 10101000 | ¿         | 168     |
| 10101001 | ⌐         | 169     |
| 10101010 | ¬         | 170     |
| 10101011 | ­         | 171     |
| 10101100 | ®         | 172     |
| 10101101 | ¯         | 173     |
| 10101110 | ¨         | 174     |
| 10101111 | ©         | 175     |
| 10110000 | ª         | 176     |
| 10110001 | ²         | 177     |
| 10110010 | ³         | 178     |
| 10110011 | ´         | 179     |
| 10110100 | µ         | 180     |
| 10110101 | ¶         | 181     |
| 10110110 | ·         | 182     |
| 10110111 | ¸         | 183     |
| 10111000 | ¹         | 184     |
| 10111001 | º         | 185     |
| 10111010 | »         | 186     |
| 10111011 | ¼         | 187     |
| 10111100 | ½         | 188     |
| 10111101 | ¾         | 189     |
| 10111110 | ¿         | 190     |
| 10111111 | ═         | 191     |
| 11000000 | ║         | 192     |
| 11000001 | ╝         | 193     |
| 11000010 | ╜         | 194     |
| 11000011 | ╓         | 195     |
| 11000100 | ╥         | 196     |
| 11000101 | ╙         | 197     |
| 11000110 | ╘         | 198     |
| 11000111 | ╒         | 199     |
| 11001000 | ╓         | 200     |
| 11001001 | ╩         | 201     |
| 11001010 | ╦         | 202     |
| 11001011 | ╠         | 203     |
| 11001100 | ═         | 204     |
| 11001101 | ╬         | 205     |
| 11001110 | ╧         | 206     |
| 11001111 | ╨         | 207     |
| 11010000 | ╤         | 208     |
| 11010001 | ╥         | 209     |
| 11010010 | ╧         | 210     |
| 11010011 | ╨         | 211     |
| 11010100 | ╪         | 212     |
| 11010101 | ╫         | 213     |
| 11010110 | ╯         | 214     |
| 11010111 | ╰         | 215     |
| 11011000 | ╱         | 216     |
| 11011001 | ╲         | 217     |
| 11011010 | ╳         | 218     |
| 11011011 | ╭         | 219     |
| 11011100 | ╮         | 220     |
| 11011101 | ╯         | 221     |
| 11011110 | ╰         | 222     |
| 11011111 | ╲         | 223     |
| 11100000 | ╳         | 224     |
| 11100001 | ╭         | 225     |
| 11100010 | ╮         | 226     |
| 11100011 | ╯         | 227     |
| 11100100 | ╰         | 228     |
| 11100101 | ╱         | 229     |
| 11100110 | ╲         | 230     |
| 11100111 | ╳         | 231     |
| 11101000 | ╭         | 232     |
| 11101001 | ╮         | 233     |
| 11101010 | ╯         | 234     |
| 11101011 | ╰         | 235     |
| 11101100 | ╱         | 236     |
| 11101101 | ╲         | 237     |
| 11101110 | ╳         | 238     |
| 11101111 | ╭         | 239     |
| 11110000 | ╮         | 240     |
| 11110001 | ╯         | 241     |
| 11110010 | ╰         | 242     |
| 11110011 | ╱         | 243     |
| 11110100 | ╲         | 244     |
| 11110101 | ╳         | 245     |
| 11110110 | ╭         | 246     |
| 11110111 | ╮         | 247     |
| 11111000 | ╯         | 248     |
| 11111001 | ╰         | 249     |
| 11111010 | ╱         | 250     |
| 11111011 | ╲         | 251     |
| 11111100 | ╳         | 252     |
| 11111101 | ╭         | 253     |
| 11111110 | ╮         | 254     |
| 11111111 | ╯         | 255     |

This table represents the characters from the extended ASCII range (128-255) in the Windows-1252 encoding. If you're using a different encoding, the characters might be different.


### Summary

While 7-bit ASCII provides a basic set of characters suitable for English and control functions, 8-bit ASCII offers a broader range of characters to support additional languages and symbols.

Note:- difference between both is only that , 8bit ASCII cover some more characters then 7bit ASCII.












