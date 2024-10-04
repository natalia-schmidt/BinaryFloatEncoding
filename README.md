# Floating-Point Representation in C (IEEE 754)

This project implements a C program to visualize the internal binary encoding of real numbers (float and double types) based on the IEEE-754 standard. It demonstrates how floating-point numbers are stored in memory, shows the system's endianness, and prints the bitwise encoding of both single-precision (`float`) and double-precision (`double`) values.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Overview

This program helps understand how real numbers are stored in memory using the IEEE-754 standard for floating-point arithmetic. It provides a binary representation of `float` and `double` types, allowing users to see how values are encoded, including the sign, exponent, and mantissa bits.

## Features

- Detects system endianness (little or big endian).
- Prints the size of `float` and `double` types in both bytes and bits.
- Allows input of a real number and converts it into binary encoding.
- Displays the binary representation of the number, including:
  - Sign bit
  - Exponent bits
  - Mantissa bits

## How It Works

The program consists of the following steps:

1. **Endianness Check**: Determines whether the system is big endian or little endian.
2. **Size Calculation**: Displays the size (in bytes and bits) of the `float` and `double` types.
3. **Input Acquisition**: Accepts a real number from the user as input.
4. **Binary Encoding**: Using pointer arithmetic, the program displays the internal binary encoding of the floating-point numbers, broken down into sign, exponent, and mantissa.

The key function used for encoding is `printEncoding`, which takes a pointer to the variable, its size, and the endianness flag.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/floating-point-representation.git
   cd floating-point-representation
   ```

2. Compile the program using a C compiler (e.g., GCC):

   ```bash
   gcc -o float_representation float_representation.c
   ```

## Usage

1. Run the program:

   ```bash
   ./float_representation
   ```

2. Follow the prompts to enter a floating-point number.

3. The program will display:
   - System endianness (Big or Little Endian)
   - Sizes of `float`, `double`, and `long double` in bytes
   - Binary encoding of the input values as `float`, `double`, and `long double`.

### Example

```
The system is: LITTLE ENDIAN
Dimensions
 af = 4 bytes
 ad = 8 bytes
 ald = 16 bytes

Insert a value (compatible with float, double, and long double): 3.14
Read: 3.140000

print float encoding:
sign bit : 0
Exponent    : 10000000
mantissa     : 10010001111010111000011

print double encoding:
sign bit : 0
Exponent    : 10000000000
mantissa     : 10010001111010111000010100011110101110000101000111101
```