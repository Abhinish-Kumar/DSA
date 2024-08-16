# Unicodes

ASCII codes are the subset of unicode take 2 byte of memory ==> 16bits.

4x4bits => represented as hexadecimal form ==> C03A

https://home.unicode.org/


## Why Unicode?

Unicode was developed to address several limitations of earlier character encoding systems. Here are the main reasons for its creation:
1. Global Character Representation:Earlier encoding systems like ASCII and EBCDIC were limited in their ability to represent characters from languages around the world. ASCII, for example, only supports 128 characters, which is insufficient for many languages and symbols.
2. Standardization Across Platforms:Different systems and platforms used various encodings (e.g., ISO 8859, Windows-1252), leading to inconsistencies and compatibility issues. Unicode provides a single, consistent encoding standard that can be used across different systems and platforms.
3. Support for All Languages:Unicode supports characters from virtually all written languages, including historical and modern scripts, as well as symbols and emojis. This ensures that text data can be shared and read correctly regardless of the language or system.
4. Handling of Multilingual Text:Unicode allows for the mixing of multiple languages and scripts within the same document or application, making it easier to handle multilingual text.
5. Backward Compatibility: Unicode was designed to be backward-compatible with ASCII. The first 128 characters of Unicode (U+0000 to U+007F) are identical to ASCII, allowing for easy integration with existing systems. (Unicode support ASCII)
6. Extensibility:Unicode is extensible, meaning it can accommodate new characters as needed. This allows it to adapt to new languages, symbols, and usage scenarios as they arise.
7. Overall, Unicode provides a comprehensive and universal encoding standard that meets the needs of a global and interconnected digital world.


| **Character** | **Code Point** | **UTF-8 Encoding** | **UTF-16 Encoding** | **UTF-32 Encoding** |
|---------------|----------------|--------------------|---------------------|---------------------|
| **Basic Latin Characters** | | | | |
| A             | U+0041         | 41                 | 0041                | 00000041            |
| **Emoji**     |                |                    |                     |                     |
| 😀             | U+1F600        | F0 9F 98 80        | D83D DE00           | 0001F600            |
| **Non-Latin Script (Japanese)** | | | | |
| こ             | U+3053         | E3 81 93           | 3053                | 00003053            |
| ん             | U+3093         | E3 82 93           | 3093                | 00003093            |
| に             | U+306B         | E3 81 AB           | 306B                | 0000306B            |
| ち             | U+3061         | E3 81 A1           | 3061                | 00003061            |
| は             | U+306F         | E3 81 AF           | 306F                | 0000306F            |
| **Mathematical Symbols** | | | | |
| ∫             | U+222B         | E2 88 AB           | 222B                | 0000222B            |



# there are so many encoding techniques so which one is used by whome or which technology


# Encoding Techniques Overview

## 1. UTF-8
- **Web Technologies:** Default for HTML and XML.
- **Programming Languages:** Used by Python, JavaScript, Ruby.
- **Operating Systems:** Supported by Windows, macOS, Linux.
- **Databases:** Employed by MySQL, PostgreSQL, MongoDB.

## 2. UTF-16
- **Windows:** Common for internal APIs and system functions.
- **Java:** Utilized for `char` type and `String` class.
- **Microsoft Office:** Formats like DOCX, XLSX.
- **XML:** Can be used, though UTF-8 is more common.

## 3. UTF-32
- **Text Processing:** Fixed-width encoding for simplified indexing.
- **Programming Languages:** Some languages or libraries use it internally.

## 4. ASCII
- **Legacy Systems:** Basic Latin characters.
- **Text Files:** Simple files and older protocols.

## 5. EBCDIC
- **IBM Mainframes:** Used for legacy data processing.

## 6. ANSI
- **Windows:** Refers to system default code pages like Windows-1252.

## 7. ISO 8859 Series
- **Legacy Systems:** Encodings such as ISO 8859-1, ISO 8859-2.

## 8. Specialized Encodings
- **Custom Encodings:** Used in specific industries or legacy systems.

**Note:** UTF-8 is widely preferred due to its compatibility with ASCII and broad character support.














