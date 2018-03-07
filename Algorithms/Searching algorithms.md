# Searching Algorithms #

## Linear Search ##

Searches in order, one by one.

## Binary Search ##

"Divide and Conquer" method; halves the search area each time an item is examined. It does, however, require the list be ordered.

```
a = [0,n-1]
found = False
low = 0
high = n
REPEAT
    middle = int((low+high/2)
    IF list[middle] = x THEN
        found = True
    ELSE
        IF list[middle] > x THEN
            high = middle - 1
        ELSE
            low = middle + 1
        END IF
    END IF
UNTIL found = True
```