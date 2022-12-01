# Chapter 1. Digital Information

Start: _November 29, 2022_<br />
Finish: _December 01, 2022_

## 1. Bits

- The smallest unit of storage
- A bit stores either a 0 or 1
- A switch that is on is represented as 0, or "false"
- A switch that is off is represented as 1, or "true"
- Anything with two seperate states can store 1 bit
- In a chip: electric charge = 0/1
- In a hard drive: spots of North/South magnetism = 0/1
- Group 8 bits together to form 1 byteu

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
  - Leftmost bit indicates sign, so carrying to the leftmost bit changes a number from positive to negative
  - Adding 1 to 2147483647 goes to -2147483648!
  - This is called **Integer Overflow**

## 4. Binary Numbers

- Binary is also known as base 2
- Base 10 is the decimal number system

### Binary Number System (1 Byte)

| n bits   | 8   | 7   | 6   | 5   | 4   | 3   | 2   | 1   |
| -------- | --- | --- | --- | --- | --- | --- | --- | --- |
| n states | 256 | 128 | 64  | 32  | 16  | 8   | 4   | 2   |

- Binary was chosen for computations as there is a trade-off between circuit complexity and efficiency
  - "zero" is any voltage less than X and "one" is any voltage more than X (Binary)
  - This makes the circuity simplistic, we do not need to worry about precision
  - In a decimal system there would need to be much more accuracy/ and or a higher voltage threshhold if 10X accuracy was not available
  - Mechanical, thermal, electrical noise all decrease accuracy
  - Binary components can be simpler, have easier circuitry, less power usage, and this makes for cheaper more reliable components

### Problems with Binary Numbers in Computers

- In General, we need to determine in advance how many bits to set aside to represent a given quantity
- If we don't set aside enough bits, we can't represent a given value
  - 7 bits can represent an age from 0 - 127
  - If somone survies past 127 years, the program is broken
- When a number in a calculation exceeds the maximum number which can be represented, we have **_overflow_**

---

> blockquote
