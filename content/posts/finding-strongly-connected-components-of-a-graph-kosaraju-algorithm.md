---
title: Finding strongly connected components of a graph (Kosaraju Algorithm)
date: 2025-10-16T09:24:00.000-06:00
weight: 0
draft: false
tags:
  - algorithms
techstack: []
cover:
  hiddenInSingle: false
---
[Github](https://github.com/jonnyjackson26/strongly-connected-components-Kosaraju)

# Kosaraju's algorithm
### Project 4 for Analysis of Algorithms
This algorithm **finds strongly connected components** in a directed graph. A strongly connected component is a portion of a graph where you can get from any one node to any other node within that portion.

The graph is stored like this in a txt file
```
1 4
2 8
3 6
4 7
```

And as problem 8.10 describes in https://www.algorithmsilluminated.org/,  *the files describe the edges of a directed graph. Vertices are labeled as positive integers from 1 to 875714. Each row indicates one edge of the graph (the tail and head vertices, in that order). For example, the eleventh row ("2 13019") indicates that there is an edge directed from vertex 2 to vertex 13019. What are the sizes of the biggest five strongly connected components?*  


To help me visualize the graph, i created create_visual_graph.py.

Then in main.py, I
1. read in the graph
2. Reverse the order of the arrows
3. Find topological ordering (Although it's not a true topo order bc in cyclic graphs thats impossible) (This is done with **Depth First Search**)
4. Then I **DFS** again, with the order I got from step 3. once you reach an end, that's how you know it's an SCC.

The idea of this works because whether or not the graph is reversed, SCCs will be the same.

## Example run:
Dataset:
```
1 4
2 8
3 6
4 7
5 2
6 9
7 1
8 5
8 6
9 7
9 3
```

![Graph](graph_curved.png)

Code:
```
myGraph = getGraph("datasets/test1.txt")
print("Original adjacency list:", myGraph)

myGraphReversed = reverseGraph(myGraph)
print("Reversed adjacency list:", myGraphReversed)

reverseTopoSortOrder = topologicalSort(myGraphReversed)
print("Topological order:", reverseTopoSortOrder)

sccs = runDFSwithReversedTopoSortOrder(myGraph, reverseTopoSortOrder)
print("SCCs:", sccs)
```

Output:
```
Original adjacency list: {1: [4], 4: [7], 2: [8], 8: [5, 6], 3: [6], 6: [9], 7: [1], 5: [2], 9: [7, 3]}
Reversed adjacency list: {1: [7], 4: [1], 2: [5], 8: [2], 3: [9], 6: [8, 3], 7: [4, 9], 5: [8], 9: [6]}
Topological order: [4, 5, 2, 8, 3, 6, 9, 7, 1]
SCCs: [[1, 4, 7], [9, 3, 6], [8, 5, 2]]
```
