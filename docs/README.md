
# DAA Assignment 1   

The paper given addresses the problem of finding the densest subgraph (DSD) in large graphs, a fundamental task in graph mining with applications in network analysis and bioinformatics. The authors introduce a core-based approach that leverages the concept of k-cores (dense subgraphs where every vertex has at least k connections) to accelerate computations.

This algorithm implemented finds the densest subgraph in an undirected graph, generalizing to cliques of size h.


Github Repository: https://github.com/imshrishk/daa_project_2

Webpage Link: https://imshrishk.github.io/daa_project_2/

## Run Locally

For Unix/Mac:

```bash
  g++ <file-name>.cpp -o <file-name>.out
  ./<file-name>.out <dataset>.txt <h>
```

For Windows:

```bash
  g++ .cpp -o <file-name>.exe
  ./<file-name>.exe <dataset>.txt <h>
```

file-name can be q1_algo1.cpp, q1_algo4.cpp  
dataset can be netscience or as733.  
h can be 2, 3 or 4.

## Contributions

The various tasks and their contributions are given below:  
1. Algorithm-1 - Abhinivesh Mitra, Sameehan Nikhil Saolapurkar
2. Algorithm-4 - Paarth Shukla, Shrish Kumar, Mohammed Kamaalullah Khan Quadri
3. Report- Abhinivesh Mitra, Sameehan Nikhil
4. Website- Mohammed Kamaalullah Khan Quadri, Shrish Kumar, Paarth Shukla
