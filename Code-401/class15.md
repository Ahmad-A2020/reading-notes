### [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html): 
Definitions: 
- Tree: A Tree is a non-linear data structure where data objects are generally organized in terms of hierarchical relationship
- Binary Tree: a binary tree is a tree data structure in which each node has at most two children, which are referred to as the left child and the right child.
  
- Node : A Tree node is a component which may contain it’s own values, and references to other nodes
- Root : The root is the node at the beginning of the tree.
-K : A number that specifies the maximum number of children any node may have.
- Left : A reference to one child node, in a binary tree
- Right : A reference to the other child node, in a binary tree
- Edge : The edge in a tree is the link between a parent and child node
- Leaf : A leaf is a node that does not have any children
- Height : The height of a tree is the number of edges from the root to the furthest leaf
 ##### Trees can be traversed in several ways: 
- Depth First Search:   Depth-first search is a type of traversal where you go as deep as possible down one path before backing up and trying a different one.
- There are several ways to perform a depth-first search: in-order, pre-order and post-order. 
    - Pre-Order Traversal: In Pre-order traversal you visit the root node first, then the left subtree,
    - Post-Order Traversal:In Post-order traversal you visit left subtree first, then the right subtree, and the root node at the end.
    - in-order traversal consists of first visiting the left sub-tree, then the root node, and finally the right sub-tree.
- Breadth First search: This type of traversal visits all the nodes of a level before going to the next level. It is like throwing a stone in the center of a pond.
- Tree types: 
  - Binary Tree: defined above
  - K-ary Trees: A tree with no more than k children for each node

  