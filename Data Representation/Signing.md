# Signing #

## Method 1: Sign bit ##

For this method, you just add an additional bit that toggles the value between being positive and negative.

0 = positive

1 = negative

Downside -requires an additional bit. Zero also has two values (0 and -0).

## Method 2: One's Compliment ##

Take the number, making sure it has a 0 as the firs t bit. For a number that has to be a negative, you just flip all the bits.

137 = 010001001

-137 = 101110110

Downside -still two values for 0!

## Method 3: Two's Compliment ##

Convert the number with a leading 0

137 = 010001001

If negative, flip the bits and add 1

-137 = 101110111

11111111 = -1 instead of -0

There are two ways to quickly get the answer.

Either:

- Make the last bit negative and then add it up.

|-128|64 |32 |16 |8  |4  |2  |1  |
|:--:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|1   |1  |1  |1  |1  |1  |1  |1  |

= -1

- Count all the 0s instead of the 1s, then add 1.

|128|64 |32 |16 |8  |4  |2  |1  |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|1  |1  |1  |1  |1  |1  |1  |1  |

= 0 + 1 = -1 

11111111 + 00000001 = 100000000

If you discard the overflow bit, the maths works (-1 + 1 = 0)
