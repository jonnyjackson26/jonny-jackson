---
title: Choosing Pivots in Quicksort
date: 2025-10-07T10:27:00.000-06:00
weight: 0
draft: false
summary: Comparing how many comparisons are required in quicksort for various
  pivot selection methods.
tags:
  - algorithms
techstack: []
cover:
  hiddenInSingle: false
---
(Github)\[https://github.com/jonnyjackson26/randomness-in-quicksort]



Comparing how many comparisons are required in quicksort if the pivot is 

1. the last element

2. the first element 

3. the median of the first, last, and middle

4. the median of 3 random elements.



In conclusion, taking the median of 3 numbers is almost always better than just one, because you reduce the likelihood that you've chosen an extreme pivot.  

The median of 3 random numbers is sometimes better than the median of the first, last, and middle element. This is interesting because introducing randomness into an algorithm makes it better which sounds counterintuitive.
