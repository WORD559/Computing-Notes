# Vectors #

## Why use vectors? ##

- Vector graphics and 3D graphics
    - Images are defined as paths, rather than as bit patterns
    - The images can then be scaled without distortion
- Computer games/simulations
    - The combination of moving forces, represented by vectors, can be resolved into a single path by using the same mathematical rules
    - For example, steering a ship against the wind and sea, calculating collision paths
- Multiple dimensions
    - Can represent 2, 3, or even more dimensions

## Definitions ##

A *scalar* quantity has magnitude only.

A *vector* quantity has both magnitude and direction.

Vectors are often written in bold to distinguish them from scalars.

## Notation ##

- Can be represented as an arrow, e.g. from (0,0) to (4,3)
- A 2-vector over ℝ, where ℝ is the set of real numbers, e.g. [4.0,3.0]
- A 3-vector over ℝ, e.g. [4.0,3.0,2.0]
- All entries from ℝ

4-vectors are also possible:

- [4.0,3.0,2.0,1.0]
- ℝ³
- All entries from ℝ
- This could be used to represent 4 dimensional spacetime, where the 4th value is time.

## Function ##

In order to translate from mathematical notation to a notation more useful in programming, we use a 'map' function.

This is NOT the same function as the `map` function in functional programming!

The notation S ⟼ ℝ means 'S maps to ℝ'

A vector can be used as a location indicator, where the set S = {0,1,2,3} maps to [2.55,-3.88,4.11,5.77]

```
0 ⟼ 2.55
1 ⟼ -3.88
2 ⟼ 4.11
3 ⟼ 5.77
```

## Exercises ##

- Represent the vector [-3,1] as an arrow.
    - [Picture](arrow.jpg)
	
## Vector Representation ##

In Python, a vector could be represented simply as a list. Alternatively, for vectors viewed as functions, it would be possible to store the vector as a dictionary.

For example, `[6.12,-7.34,-8.45]` or `{0:6.12,1:-7.34,2:-8.45}`

## Vector Calculations ##

This is the same as the crap from C4/M1/Physics

### Vector Addition ###

- (a + b) is found by reloacting b so that the hea touches the tail (translation)
- The x and y (or i and j) components of the vectors are added separately to make a new vector
- For example, [4,0] + [3,4] = [7,4].
    - [This can be shown graphically](headtail.jpg)
	
### Finding the Magnitude ###

- The magnitude of a vector (also written as, for example, |v|) is found by √(x²+y²)
- Think Pythagoras.

### Scalar Multiplication (Scaling) ###

- Multiplying a vector by a scalar value changes the magnitude of the vector
- You simply multiply each element of the vector by the scalar
   - [This can also be shown graphically](multiply.jpg)
   
## Convex Combination of Vectors ##

- The convex combination of two vectors is the space bounded between the vectors.
- Mathematically,
to perform a convex combination, you will be multiplying one vector either by a scalar, or
by another vector.
- It is an expression in the form w = αu + βv

They are useful for 3D modelling, for example calulating the volume of a polyhedra. They can also be used to show models with perspective.

### Example ###

u = (2,2), v = (6,-2), w = ½u + ½v

w = (1+3,1-1) = (4,0)

## Dot Product ##

- The dot product of two vectors is acquired by multiplying each part of the vector together and summing the results.
- This is useful to us because we can use this to find the angle between two vectors, because the dot product can also be defined as the product of the magnitudes and the cosine of the angle between the two vectors.
- Therefore, cos = (u•v)/(|u|•|v|)