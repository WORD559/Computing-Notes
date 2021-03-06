```
A = {2,4,6,8,10}
B = {Multiples of three less than 12}
C = {2,3,5,7,11,13,17,19}
D = {4,6,8}
E = {}
F = {4,6,8}
```

- \ = Difference
- ∪ = Union
- ∩ = Intersection
- ⊂ = Proper subset of
- ⊆ = Subset of
- ∈ = element of
- ∉ = not an element of

This translates to:

- A\B = A - B = {2,4,8,10}
- A∪B = A OR B = {0,2,3,4,8,9,10}
- A∩B = A AND B = {6}
- D⊂A = A contains D = {
- F⊆D = D contains or is equal to F

-----------------

- ℕ = Natural Numbers
- ℤ = Integers
- ℚ = Quotient (rational numbers)
- ℝ = Real
- 𝕀 = Imaginary
- ℂ = Complex (bits of imaginary, bits of real)

These are all proper subsets of each other

- ℕ ⊂ ℤ
- ℤ ⊂ ℚ
- ℚ ⊂ ℝ
- ℝ ⊂ ℂ
- 𝕀 ⊂ ℂ


What if we want a set of even numbers less than 1,000,000?

`A = {2x | x∈ℕ ∩ x≤500,000}`


All the numbers divisible by 4? `A = {4x | x∈ℤ}`

This is a countably infinite set. 


`(B\A) + (A\B)` can be simplified to `A⊕B`