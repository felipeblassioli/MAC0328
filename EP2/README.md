# [2-Approximation to Metric TSP](http://en.wikipedia.org/wiki/Travelling_salesman_problem#Metric_TSP)

## [Algorithm](http://en.wikipedia.org/wiki/Travelling_salesman_problem#Metric_TSP)

  1. Construct a minimum spanning tree T for G.
  2. Duplicate all edges of T. That is, wherever there is an edge from u to v, add a second edge from v to u. This gives us an Eulerian graph H.
  3. Find an Eulerian circuit C in H. Clearly, its span is twice the span of the tree.
  4. Convert the Eulerian circuit C of H into a Hamiltonian cycle of G in the following way: walk along C, and each time you are about to come into an already visited vertex, skip it and try to go to the next one (along C).

## Input and Output

The first line of the input is n (the number of vertices in the complete graph G).
The following n lines have n integers separetd by whitespace with the cost of the edge.

The last line of the output is the hamiltonian path that approximates the minimum path cost. (the 2-approximation).
The previous lines are the edges of the MST.

**Sample Input:**

```
4
0 6 3 5
6 0 4 8
3 4 0 5
5 8 5 0
```

**Sample Output:**

```
0 2
1 2
2 3
0 2 1 3 0
```