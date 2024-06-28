# Vertex Ordering Optimization

This repository contains the implementation of various search algorithms (BFS, DFS, UCS, and Greedy) to find the optimal ordering of vertices in a network, minimizing the total cost of the network. This project is inspired by the optimization problem commonly found in Bayesian Network Learning.

## Table of Contents

- [Introduction](#introduction)
- [Data Format](#data-format)
- [Usage](#usage)
- [Algorithms](#algorithms)
- [Example](#example)
- [License](#license)

## Introduction

The goal of this project is to determine a vertex ordering with the minimum cost given a set of vertices and their possible parent sets with associated costs. The problem can be simplified as finding a vertex ordering that minimizes the total cost of the network.

## Data Format

The input data is provided in text files where each line represents a vertex, its parent set, and the associated cost. The format of each line is as follows:
```
vertex, {parent_set}, cost
```

Example:
```
1,{},153.466
1,{3},96.093
1,{4},97.913
1,{5},99.835
2,{},141.023
...
```

## Usage

To run the search algorithms on the provided datasets, execute the following command:
```
python VertexOrderingOptimization.py
```

## Algorithms

### Breadth-First Search (BFS)
BFS explores all possible orderings level by level and finds the minimum cost ordering by visiting each vertex exactly once.

### Depth-First Search (DFS)
DFS explores each possible ordering path to its depth, backtracking when a complete ordering is found, and finds the minimum cost ordering.

### Uniform Cost Search (UCS)
UCS explores the search space similar to BFS but prioritizes paths with lower costs using a priority queue.

### Greedy Search
Greedy search selects the next vertex that leads to the lowest cost incrementally until all vertices are ordered.

## Example

Consider the ordering (5, 3, 1, 4, 2). With respect to vertex 1, the parent set {4} is not consistent with the ordering. The parent sets {}, {3}, and {5} are consistent with the ordering. The ordering (5, 3, 1, 4, 2) has a total cost of 465.435.

### Running the Example

1. Place your data files (e.g., `data0.txt`, `data1.txt`, `data2.txt`) in the project directory.
2. Execute the script to process the files and find the optimal ordering:
   ```
   python main.py
   ```
3. The script will output the orderings and their costs for each dataset.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
