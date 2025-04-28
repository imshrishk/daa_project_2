# CS F364 Assignment Report

## Group 51

- Sameehan Nikhil Saolapurkar (2022A7PS1359H)
- Paarth Shukla (2022A7PS1287H)
- Abhinivesh Mitra (2022A7PS1311H)
- Shrish Kumar (2022A7PS1295H)
- Mohammed Kamaalullah Khan Quadri (2022A7PS0109H)

## Introduction

The paper given addresses the problem of finding the densest subgraph (DSD) in large graphs, a fundamental task in graph mining with applications in network analysis and bioinformatics. The authors introduce a **core-based approach** that leverages the concept of *k-cores* (dense subgraphs where every vertex has at least *k* connections) to accelerate computations.

This algorithm implemented finds the densest subgraph in an undirected graph, generalizing to cliques of size h (default h=2, i.e., edges). The main steps are:

* **Clique Enumeration:** It first enumerates all (h−1)-cliques in the graph. For h=2, these are just the vertices; for larger h, it finds all cliques of size h−1.
* **Clique Degree Calculation:** For each vertex, it calculates the number of (h−1)-cliques it can extend to a full h-clique, storing this as the "clique degree."
* **Binary Search on Density:** The algorithm performs a binary search over possible density values (number of h-cliques per vertex) to find the maximum achievable density.
* **Max-Flow Construction:** For each candidate density, it constructs a flow network where capacities are based on clique degrees and the candidate density. It then runs the Ford-Fulkerson algorithm to compute the maximum flow.
* **Minimum Cut Extraction:** If the maximum flow is insufficient, it extracts the minimum cut in the flow network to identify the set of vertices forming the densest subgraph.
* **Density Calculation:** Finally, it computes and reports the density of the found subgraph as the number of h-cliques divided by the number of vertices in the subgraph.

This approach generalizes the classic densest subgraph problem (where h=2) to larger cliques.

## Results

### Dataset: NetScience

#### Densest Subgraph Result:

| Size of the clique | Density | Number of vertices |
|-------------------|---------|-------------------|
| 2                 | 9.5     | 20                |
| 3                 | 57      | 20                |
| 4                 | 242.25  | 20                |

### Dataset: as733

| Size of the clique | Density | Number of vertices |
|-------------------|---------|-------------------|
| 2                 | 8.875   | 40                |
| 3                 | 35.9    | 33                |
| 4                 | 85.125  | 32                |
