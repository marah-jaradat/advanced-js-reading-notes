# 26-March-2022- 13th class reading notes:

## Trees:

### **Introduction**

The key feature of the tree structure is that it is recursive . In other words, a tree consists of subtrees, which in turn consist of subtrees, which in turn … In the end, at the very bottom, there are leaves — and now they have no descendants and do not lead anywhere.
A tree consists of nodes and edges between them. The ribs in reality do not exist, they are needed only to visualize the connection and, if necessary, to describe it. Nodes are divided into two types: internal (those that have descendants) and leaf nodes (those that have no descendants). In the case of a file system, leaf nodes are represented by files, and internal ones are directories.

Definition
The number of ways to describe trees is infinite. Here we consider only those that are based on the repetition of the tree structure in the data structure that describes it. 

**Common Terminology**

- Node : A Tree node is a component which may contain its own values, and references to other nodes
- Root: The root is the node at the beginning of the tree
- K : A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left : A reference to one child node, in a binary tree
- Right: A reference to the other child node, in a binary tree
- Edge : The edge in a tree is the link between a parent and child node
- Leaf : A leaf is a node that does not have any children
- Height : The height of a tree is the number of edges from the root to the furthest leaf

![Binary tree](./maxresdefault%20(1).jpg)
**Traversals**
An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:

- Depth First
- Breadth First

**Binary Tree Vs K-ary Trees**
In all of our examples, we’ve been using a Binary Tree. Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows. 

**K-ary Trees**
If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use K to refer to the maximum number of children that each Node is able to have.

A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree. Height can be calculated as log n, where n is the number of nodes.

### Useful links

* [intro to trees](https://medium.com/@iampika/javascript-trees-b8f3b4261c3a)


* [video of trees](https://www.youtube.com/watch?v=qH6yxkw0u78&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=26)


* [tutorial of three parts about trees](https://www.youtube.com/watch?v=r8drVrKgVZk)