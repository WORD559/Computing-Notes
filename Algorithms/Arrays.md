# Arrays #

If you need to sort, for example, 100 town names into alphabetical order, it is inconvenient to have different variable names to hold each one.

|Name 1|Name 2|0  |1  |2  |i  |OUTPUT|
|:----:|:----:|:-:|:-:|:-:|:-:|:----:|
|Joe   |Jim   |Moe|Mae|Mic|0  |Moe   |
|Joe   |Jim   |Moe|Mae|Mic|1  |Mae   |
|Joe   |Jim   |Moe|Mae|Mic|2  |Mic   |
|Joe   |Jim   |Moe|Mae|Mic|2  |Joe   |
|Joe   |Jim   |Moe|Mae|Mic|2  |Jim   |

It is easier to store them all under one variable name and assign them all an index.

