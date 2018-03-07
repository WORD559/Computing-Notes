# Sorting Algorithms #

- Sorting is a very common operation in data processing
- There are many different sorting algorithms, from very simple ones that execute very slowly (e.g. bubble sort) to more complex ones which execute very fast (e.g. Merge sort).

## Bubble Sort ##

The bubble sort gets its name from being like bubbles in a glass of water - items "float" to the top as they are sorted. It is quite slow, as it goes through all n items in the list n times. 

To perform the bubble sort, start at one end of the list and go along it. At each item in the list, you compare it with the next item. If the current item is greater than the next item, you swap them.

After n iterations through the list, the last n items at the end of the list will be sorted. This allows you to optimise the algorithm slightly by not going as deep into the list each time.

Another way to optimise the bubble sort is to use a boolean flag that states whether two items have been swapped on the current iteration. If this flag is still `false` at the end of the current iteration, then the list is now sorted and the algorithm can terminate.

The bubble sort is useful for when only a small number of items need to be sorted.

## Merge Sort ##

The merge sort works by merging lists together, hence its name. First of all, the list to be sorted is split in half repeatedly until the original list has been broken down into lots of lists with length 1. Because they all have length 1, we can say that all of these lists are sorted. These lists are then recombined with their other halves by comparing the first elements of each list. The smallest of the two first elements is appended to the new list and removed from its original list. Since the two lists being merged are always ordered, this process of recombining sorts the list.

The merge sort is, along with the quicksort, one of the fastest sorting algorithms. It is much faster than the bubble sort, especially as the length of the list increases