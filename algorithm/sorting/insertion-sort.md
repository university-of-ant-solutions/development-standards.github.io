---
description: Insertion Sort Algorithm
keywords: algorithm, sorting, insertion sort
title: Insertion sort Algorithm
---

## Insertion Sort Algorithm

Now we have a bigger picture of how this sorting technique works, so we can derive simple steps by which we can achieve insertion sort.

```
Step 1 − If it is the first element, it is already sorted. return 1;
Step 2 − Pick next element
Step 3 − Compare with all elements in the sorted sub-list
Step 4 − Shift all the elements in the sorted sub-list that is greater than the
         value to be sorted
Step 5 − Insert the value
Step 6 − Repeat until list is sorted
```

## Pseudocode

```
procedure insertionSort( A : array of items )
   int holePosition
   int valueToInsert

   for i = 1 to length(A) inclusive do:

      /* select value to be inserted */
      valueToInsert = A[i]
      holePosition = i

      /*locate hole position for the element to be inserted */

      while holePosition > 0 and A[holePosition-1] > valueToInsert do:
         A[holePosition] = A[holePosition-1]
         holePosition = holePosition -1
      end while

      /* insert the number at hole position */
      A[holePosition] = valueToInsert

   end for

end procedure
```

## Demo

- [Implement in JS](https://github.com/university-of-ant-solutions/ecmascript-training/blob/develop/source/src/sorting-techniques/insertion-sort/index.js#L1)

## Resources

* [https://www.tutorialspoint.com/data_structures_algorithms/insertion_sort_algorithm.htm](https://www.tutorialspoint.com/data_structures_algorithms/insertion_sort_algorithm.htm)
* [http://www.geeksforgeeks.org/insertion-sort/](http://www.geeksforgeeks.org/insertion-sort/)
