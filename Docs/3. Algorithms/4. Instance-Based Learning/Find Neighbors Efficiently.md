# Find Neighbors Efficiently

## Problem

Given a set of points in a 2D plane, find the k closest points to a given point.

## Sequential Table

- Compute the distance between the given point and all other points.
- O(n) time complexity with a sequential scan.

## Binary Tree

### kD-Tree

- A binary tree in which every node is a k-dimensional point.
- Every non-leaf node generates a splitting hyperplane that divides the space into two half-spaces.
- The left subtree contains points on the "left" side of the hyperplane, and the right subtree contains points on the "right" side.
- The root node is the median point of the set of points.
- The tree is constructed recursively by selecting the median point of the set of points as the root node and recursively building the left and right subtrees.
- The tree is balanced, and the height is O(log n).
- The time complexity of finding the k closest points is O(log n).

### Ball Tree

- A binary tree in which every node is a ball that contains a set of points.
- The root node is the smallest ball that contains all points.
- The tree is constructed recursively by selecting a point that is farthest from the center of the ball as the root node and recursively building the left and right subtrees.
- The tree is balanced, and the height is O(log n).
- The time complexity of finding the k closest points is O(log n).

## Hash Table

### Locality-Sensitive Hashing (LSH)

- A hash table can be reated by projecting the data onto a line and discretizing the projection into bins.
- We choose l random projections and create l hash tables.
- Given a query point $x_q$, we fetch the set of points in bin $g_k(x_q)$ for each hash table $k$.
- The union of the sets of points from all hash tables is the set of candidate points.
- We find the k closest points from the candidate points.
- The time complexity of finding the k closest points is O(1) with high probability.
