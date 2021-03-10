# ![basepack](https://github.com/mrmartin/basepack/raw/master/basepack2.png)
Dataset of 2D polygons and 3D polytopes to benchmark packing algorithms. Polytope packing is the problem of how to place objects so that they take up least space.

[![example packing](https://github.com/mrmartin/basepack/raw/master/packing.png)](https://www.youtube.com/watch?v=PCxPIBJEEyU)

## description
The 2D polygons have a variable number of edges, and 3D polyhedra have a variable number of faces (TBD). Both have variable scale, and the code to generate these is provided.

Baseline packings are also available for each dataset, for reference, including code. (TBD)

Two packing-efficiency metrics are also provided: fit in smallest rectangle/cuboid, and fit in convex hull. (TBD)

Higher-dimensional polytopes are not included, but the code enables the creation of convex polytopes of any dimension.

## data
This repository contains 8 datasets of 2D and 3D polytopes, as follows:

1. 2D rectangles
2. 2D convex polygons
3. 2D non-convex polygons
4. 2D rectanges + convex + non-convex
5. 3D cuboids (boxes)
6. 3D convex polytopes
7. 3D non-convex polytopes
8. 3D cuboids + convex + non-convex

For each of the types of polytope being generated, there are two free parameters: 
* random seed
* number of polytopes

the following hyperperameters are fixed: 

* scale range
* number of edges range

Each 2D dataset is a csv file, where each line corresponds to a single polygon. Each line contains an even number of 5-decimal place doubles, describing points x_1, y_1, x_2, y_2, ..., such that they are ordered for traversal.

Each 3D dataset is a folder, in which each stl file corresponds to a polyhedron.

## usage
To benchmark a packing algorithm with statistical significance, generate your relevant dataset by increasing the ``dataset_random_seed`` parameter (0 to bignum), and to benchmark algorithms for speed, increase the size of datasets with the ``dataset_size`` parameter (1 to bignum).
