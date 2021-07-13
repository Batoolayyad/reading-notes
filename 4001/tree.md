
### Terminology
* Tree node: is a component contain it’s own values, and references to other nodes
* root : the node at the beginning of the tree
* K: the maximum number of children any node may have in a k-ary tree. 
* Edge: The edge in a tree is the link between a parent and child node
* Leaf: A leaf is a node that does not have any children
* Height: The height of a tree is the number of edges from the root to the furthest leaf
* In a binary tree we have left that has reference to one child node and Right that had reference to the other child node. Also in a binary tree, k = 2.



### Depth First

#### Pre-order: root >> left >> right
#### In-order: left >> root >> right
#### Post-order: left >> right >> root

### Traversal Pseudocode
#### pseudocode for all three of the depth first traversals:

##### Pre-order
```
ALGORITHM preOrder(root)
// INPUT <-- root node
// OUTPUT <-- pre-order output of tree node's values

    OUTPUT <-- root.value

    if root.left is not Null
        preOrder(root.left)

    if root.right is not NULL
        preOrder(root.right)
```
#### In-order
```
ALGORITHM inOrder(root)
// INPUT <-- root node
// OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)
```
#### Post-order
```
ALGORITHM postOrder(root)
// INPUT <-- root node
// OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value
```


## Binary Search Trees


- A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. 
- In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.


### Big O


The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.
The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.


