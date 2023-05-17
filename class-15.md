# Class 15 - Trees

## What is tree?

A tree data structure is a hierarchical structure that is used to represent and organize data in a way that is easy to navigate and search. It is a collection of nodes that are connected by edges and has a hierarchical relationship between the nodes.

You can think of it like family trees, organizing information hierarchically and allowing efficient access to data, just as family trees help us trace our lineage and relationships

### In Depth

A tree is a nonlinear data structure, compared to arrays, linked lists, stacks and queues which are linear data structures. A tree can be empty with no nodes or a tree is a structure consisting of one node called the root and zero or one or more subtrees.

A tree can be explained as a collection of nodes connected by edges. Nodes without children are called leaf nodes or external nodes. Nodes with at least one child node are called internal nodes. An edge in a tree is a connection between two nodes. This connection shows the relationship between the nodes. Every node (excluding a root) in a tree is connected by a directed edge from exactly one other node. This node is called a parent. On the other hand, each node can be connected to arbitrary number of nodes, called children. Nodes with the same parent are called siblings.

![tree](assets/img/Treedatastructure.png)

## why we use tree?

Other data structures such as arrays, linked list, stack, and queue are linear data structures that store data sequentially. In order to perform any operation in a linear data structure, the time complexity increases with the increase in the data size. But, it is not acceptable in today's computational world.

Different tree data structures allow quicker and easier access to the data as it is a non-linear data structure. The data is stored in a hierarchical manner in tree structures. The time complexity of tree data structures (searching, inserting, and deleting) is much lesser as compared to other data structures.

## Binary Trees

A binary tree is a tree data structure in which each node has at most two children, which are referred to as the left child and the right child.

### Binary Search Trees

A binary search tree is a binary tree in which every node fits a specific ordering property: all left descendents <= n < all right descendents. This must be true for each node n.

![Binary Search Trees](assets/img/binary-search-tree-sorted-array-animation.gif)
