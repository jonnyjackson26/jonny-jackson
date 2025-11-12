---
title: Using Branch and Bound to solve 0/1 Knapsack Problem
date: 2025-11-12T15:33:00.000-07:00
weight: 0
draft: false
summary: Using Branch and Bound to solve 0/1 Knapsack Problem
tags:
  - algorithms
techstack: []
cover:
  hiddenInSingle: false
---
https://github.com/jonnyjackson26/knapsack-branch-and-bound

Solving https://www.algorithmsilluminated.org/ problem 16.7

In this problem, each file describes an instance of the knapsack problem and has the format:
\[knapsack_size]
\[value_1] \[weight_1]
\[value_2] \[weight_2]
...
You can assume that all numbers are positive. You should assume that item weights and the knapsack capacity are integers.
Test case: What is the value of an optimal solution to the knapsack instance described in this file? (Answer: 2493893)
Challenge data set: Repeat the previous problem for the knapsack instance described in this file. This instance is so big that the straightforward iterative implementation described in the book uses an infeasible amount of time and space. So you will have to be creative to compute an optimal solution. One idea is to go back to a recursive implementation, solving subproblems --- and, of course, caching the results to avoid redundant work --- only on an "as needed" basis. Also, be sure to think about appropriate data structures for storing and looking up solutions to subproblems.

The idea is you branch and bound, so you only go down a tree if it fits a "bound". In this case, the bound is th fractional knapsack with can be solved in n log n.
