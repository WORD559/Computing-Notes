# Fractions #

## Fixed Point ##

Since binary goes up in powers of two, why can't it also go down?

|8  |4  |2  |1  |1/2|1/4|1/6|1/8|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|0  |1  |1  |0  |1  |1  |0  |0  |

So if we wanted to convert 6.75 to binary, we would do the following:

|2  |1  |1/2|1/4|1/8|1/16|1/32|1/64|
|:-:|:-:|:-:|:-:|:-:|:--:|:--:|:--:|
|1  |1  |1  |0  |1  |1   |0   |1   |

An easy way to convert into binary is as follows:

3.703125 = 11.?

1. Take off the decimal part: 0.703125
2. Multiply by two: 1.406250
3. Take off the decimal again: 0.406250
4. Multiply by two: 0.81250
5. Repeat until it equals 1
6. String them together: 101101

0.8125 * 2 = 1.625

0.625 * 2 = 1.25 

0.25 * 2 = 0.5 

0.5 * 2 = 1

2 + 1 + 0.5 + 0.125 + 0.0625 + 0.015625 = 3.703125

-------------------

However, not ALL numbers can be represented accurately.

1.45 or 1.3, for example, would create a recurring set.

## Floating Point ##

Floating points are based on scientific standard form, except instead of m * 10^e, we use m * 2^e

m = mantissa, two's compliment fixed point

e = exponenet, two's compliment integer

For example:

10101000000000101

m = 1.010100000

e = 000101

The least significant 1 bit is at 1/16

|-1 |.5 |.25|.125|.0625|
|:-:|:-:|:-:|:--:|:---:|
|1  |0  |1  |0   |1    |
	
We can find out its value as if it were:

|-16|8  |4  |2  |1  |
|:-:|:-:|:-:|:-:|:-:|
|1  |0  |1  |0  |1  |
	
Which is 11.

So the answer is 11x2^e

We then find e normally (e = 5) and add, in this example, log2(1/16) = -4 

5 + -4 = 1, so the answer is 11x2^1 = 22 

-------------

In order to maximise storage in the number, they should be normalised. For this, you the first two bits should alternate (i.e. 10 or 01)

To convert to floating point, consider the following example.

27 5/8 -> 8,4 floating point

27 5/8 = 011011.101

011011.101 -> 0.1101110(1)

011011.101 = 0.1101110(1) x 2^5

5 = 0101

27 5/8 = 01101110 0101

We've lost a bit here, so instead of storing 27 5/8, we have stored 27 1/2. There is an error of 1/8.

For this we use Relative Error -the amount of error we have relative to the size of the number we're storing.

So in this instance, we have (1/8) / 27 5/8

-------------

Even though you're storing data in this way, there is still a limit on the number of unique values you can store.

If you're storing the mantissa in 6 bits and the exponent in 4, you're using 10 bits in total. Therefore there are 2^10 different combinations you can have. Using that configuration, you can therefore only store 1024 different numbers.
