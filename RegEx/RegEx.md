# Regular Expressions (RegEx) #

We want to validate names.

- Dave - valid
- Bob - valid
- K1tty - invalid (number)
- John Clifton - invalid (space)
- aggghhhh! - invalid (punctuation)
- ohpoo - valid

The regular expression to validate this would be [a-zA-Z]+

What does this mean?

|Token  |Definition                               |
|:-----:|-----------------------------------------|
|`.`    | an occurance of something               |
|`?`    | zero or one occurance of preceding      |
|`+`    | one or more occurances of preceding     |
|`*`    | zero or more occurances of the preceding|
|`[ ]`  | allowable characters                    |
|`\|`    | OR                                      |
|`( )`  | just brackets                           |
|`-`    | range (e.g. A-Z)                        |
|`^`    | NOT                                     |
|`\`    | escape                                  |
|`{n}`  | exactly n copies of                     |
|`{n,}` | at least n copies of                    |
|`{n,m}`| between n and m copies of               |

`(0|(1(01*0)*1))*`

zero or more of 0 or (zero or more of (0(zero or more of 1)0))1)
 
If interpreted as binary unsigned integers, these are multiples of three!
