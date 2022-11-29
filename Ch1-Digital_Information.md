# Chapter 1. Digital Information

## 1. Bits

- The smallest unit of storage
- A bit stores either a 0 or 1
- Anything with two seperate states can store 1 bit
- In a chip: electric charge = 0/1
- In a hard drive: spots of North/South magnetism = 0/1
- Group 8 bits together to form 1 byte

  ### How Many Patterns with N Bits?

  | Number of bits | Different Patterns                   |
  | -------------- | ------------------------------------ |
  | 1              | 0 1                                  |
  | 2              | 00 01 10 11                          |
  | 3              | 000 001 010 011<br />100 101 110 111 |

  ### In general: add 1 bit, double the # of patterns

  | Number of bits | Number of patterns |
  | -------------- | ------------------ |
  | 1              | 2                  |
  | 2              | 4                  |
  | 3              | 8                  |
  | 4              | 16                 |
  | 5              | 32                 |
  | 6              | 64                 |
  | 7              | 128                |
  | 8              | 256 (one byte)     |

## 2. Bytes

- A byte is a unit of information storage
- One Byte = a collection of 8 bits
- e.g. 0 1 0 1 1 0 1 1
- One byte can store one character, e.g. 'A' or 'x' or '$'
- 8 bits can make up to 256 different patterns
- One byte can hold a number between 0 & 255
- All storage is measured in bytes, despite being very different hardware
  - kilobyte, KB, 1E3 bytes
  - Megabyte, MB, 1E6 bytes
  - Gigabyte, GB, 1E9 bytes
  - Terabyte, TB, 1E12 bytes
- ASCII is an encoding representing each typed character by a number
  - A is 65
  - B is 66
  - a is 69
  - space is 32
- "Unicode" is an encoding for mandaring, greek, arabic, etc. languages, typically 2-bytes per "chracter"
- Each letter is stored in a byte, as below
  | s | p | r | i |
  | - | - | - | - |
  | 83 | 112 | 114 | 105 |
- 100 typed letters takes up 100 bytes
- when you send text messages, the bytes are sent
- text is quite compact, using few bytes, compared to images etc.

## 3. Numbers in Computers

- **Integers** are typically stored with either 4 or 8 bytes
- 4 bytes can store numbers between -2147483648 and 2147483647
- 8 bytes can store numbers between -9223372036854775808 and 9223372036854775807
- Adding in binary is just like normal addition with carrying
  - When you run out of bits you cannot carry anymore
  - Leftmost bit indicates sign, so carrying to the leftmost bit changes a number from positive to negative.
  - Adding 1 to 2147483647 goes to -2147483648!
  - This is called **Integer Overflow**

---

> blockquote
