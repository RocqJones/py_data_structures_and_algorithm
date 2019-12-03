# py_data_structures_and_algorithm 🔥
Problem Solving with Data Structures and Algorithms using Python. 

Let's make it interesting

#### Algorithms + Data Structures = Programs

To answer why DSA are important? It's because, they are what you do after you've become a computer scientist... As you can guess, the most we can optimize is the 2nd step, which is where we have Data structures and algorithm.

## Types of Data Structures.
### 1. Linked List.
* It's a linear data structure where each element is a separate object. Each element (we will call it a node) of a list is comprising of two items - the data and a reference to the next node. The last node has a reference to null. The entry point into a linked list is called the head of the list.

### 2. Binary Search Tree Algorithm.
* The recursive structure of a BST yields a recursive algorithm. Searching in a BST has ```O(h)``` worst-case runtime complexity, where h is the height of the tree. Since s binary search tree with n nodes has a minimum of ```O(log n)``` levels, it takes at least ```O(log n)``` comparisons to find a particular node.

#### Binary Search Tree, is a node-based binary tree data structure which has the following properties:
- The left subtree of a node contains only nodes with keys lesser than the node’s key.
- The right subtree of a node contains only nodes with keys greater than the node’s key.
- The left and right subtree each must also be a binary search tree.
- There must be no duplicate nodes.
 
![BSTSearch](BSTSearch.png)

### 3. AVL Trees (Adelson-Velskii and Landis)
AVL tree is a self-balancing Binary Search Tree (BST) where the difference between heights of left and right subtrees cannot be more than one for all nodes. An Example Tree that is an AVL Tree. The above tree is AVL because differences between heights of left and right subtrees for every node is less than or equal to 1.

#### Insertion
To make sure that the given tree remains AVL after every insertion, we must augment the standard BST insert operation to perform some re-balancing. Following are two basic operations that can be performed to re-balance a BST without violating the BST property (keys(left) < key(root) < keys(right)).
1) Left Rotation
2) Right Rotation
#### Steps to follow for insertion
Let the newly inserted node be w
1) Perform standard BST insert for w.
2) Starting from w, travel up and find the first unbalanced node. Let z be the first unbalanced node, y be the child of z that comes on the path from w to z and x be the grandchild of z that comes on the path from w to z.
3) Re-balance the tree by performing appropriate rotations on the subtree rooted with z. There can be 4 possible cases that needs to be handled as x, y and z can be arranged in 4 ways. Following are the possible 4 arrangements:
* y is left child of z and x is left child of y (Left Left Case)
* y is left child of z and x is right child of y (Left Right Case)
* y is right child of z and x is right child of y (Right Right Case)
* y is right child of z and x is left child of y (Right Left Case)
```
T1, T2 and T3 are subtrees of the tree 
rooted with y (on the left side) or x (on 
the right side)           
     y                               x
    / \     Right Rotation          /  \
   x   T3   - - - - - - - >        T1   y 
  / \       < - - - - - - -            / \
 T1  T2     Left Rotation            T2  T3
Keys in both of the above trees follow the 
following order 
 keys(T1) < key(x) < keys(T2) < key(y) < keys(T3)
So BST property is not violated anywhere.
```
Another example of self-balancing tree.
![AVL_Insertion](AVL_Insertion.jpg)
