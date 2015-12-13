# ISTE-190 - Number Systems

## Positional number systems
* Positional number system defined by:
 * A base
 * Set of numeric symbols that take form of numbers / alphabetic symbols
 * Value that each symbol represents depends on place value (i.e. base raised to exponent)
* *Example*: Decimal number system
 * Base 10
 * 10 symbols {0,1,2,3,4,5,6,7,8,9}
 * Place values = powers of 10

![Example of decimal system](https://i.j-f.co/u/49ea8e0aeb0e68f29c0d11d1a3933532.png)

## Number systems in computing
* Two common systems in computing:
 * Binary
 * Hexadecimal
* Binary
 * Base 2
 * 2 symbols {0,1}
 * Place values = powers of 2
* Hexadecimal
 * Base 16
 * 16 symbols {0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F}
 * Place values = powers of 16

![Example of binary system](https://i.j-f.co/u/1fa387ffcc801042e4efda7537d87f00.png)
![Example of hexadecimal system](https://i.j-f.co/u/6e32b7b59c991229fc398f4836991d1e.png)

## Converting: Binary => Hexadecimal
* Hexadecimal is shorthand notation for groups of binary digits
* Each group of four binary digits represented by one hex character
* Examples
 * Decimal 15 = Binary 1111 = Hex F
 * Decimal 128 = Binary 1000 0000 = Hex 80
 * Decimal 255 = Binary 1111 1111 = Hex FF

## Converting: Decimal => Binary / Hexadecimal
* Method process:
 * Divide the decimal number by number system base
 * Record quotient and remainder
 * Continue until quotient is zero
 * Remainders in bottom-to-top order represent converted value
* [Number system converter](http://www.mathsisfun.com/binary-decimal-hexadecimal-converter.html)

## Binary Digit (Bit)
* *Bit*: Basic unit of information in computer
* Can physically represent symbol in the binary number system
* Sequences of bits form bit patterns
* Interpretation of bit pattern depends on context
* **All information can be represented by string of digits {0,1}**

### Using bits
* Given N bits:
 * Number of unique bit patterns = 2^N
 * Highest value = (2^N) - 1
* *Example*: Given three bits…
 * Number of unique bit patterns = 2^3 = 8
 * High value = (2^3) - 1 = 7

### Spaces
* Space is collection of unique things
* Number of things in a space is determined by bits used to define space
* Common spaces:
 * CPU memory address space
 * IP address space
 * Key space
 * RGB color space