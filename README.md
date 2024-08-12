![MATLAB](https://img.shields.io/badge/MATLAB-%23D00000.svg?style=plastic&logo=mathworks&logoColor=white)  ![GitHub](https://img.shields.io/github/license/Ramy-Badr-Ahmed/KD-Tree-Matlab?style=plastic)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.12808902.svg)](https://doi.org/10.5281/zenodo.12808902)

# KD-Tree Implementation in MATLAB

This repository contains MATLAB scripts for implementing and using a kd-tree data structure and implements k-nearest neighbour search.

The kd-tree is a space-partitioning data structure for organising points in a k-dimensional space.

### About

   > [Mathematica Link](https://reference.wolfram.com/language/ref/datastructure/KDTree.html)

### Scripts

1. `buildKDTree.m`

   > Builds a kd-tree from a set of points.

2. `nearestNeighborSearch.m`

   > Performs nearest neighbour search using the built kd-tree.

3. `hypercubePoints.m`

   > Showcases an application to generate n-Dimensional Points Uniformly in an n-Dimensional Hypercube.


### Example Usage

```matlab
numPoints = 5000;
cubeSize = 10;
numDimensions = 10;

points = hypercubePoints(numPoints, cubeSize, numDimensions);

hypercubeKDTree = buildKDTree(points);

queryPoint = rand(1, numDimensions);  % for the k-nearest neighbour search

[nearestPoint, nearestDist, nodesVisited] = nearestNeighbourSearch(hypercubeKDTree, queryPoint);

fprintf('Points in KD-Tree:\n');
fprintf('Query point: (%.2f, %.2f, %.2f)\n', queryPoint);
fprintf('Nearest point: (%.2f, %.2f, %.2f)\n', nearestPoint);
fprintf('Distance: %.4f\n', nearestDist);
fprintf('Nodes visited: %d\n', nodesVisited);
```
