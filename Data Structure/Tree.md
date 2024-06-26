# Tree
- A hierarchical data structure in which a collection of elements known as nodes are connected to each other via edges.

# Concepts of Tree
<div align="center">
  <img src="https://github.com/TIBBOH17/CS/assets/121493257/ca52a34e-4b5e-48e6-9716-99bec4b75709" width="50%", alt="">
</div>

#### Root Node
- The topmost node of a tree or the node which does not have any parent node.

#### Leaf Node
- The nodes which do not have any child nodes.

#### Parent Node
- The node which is a predecessor of a node.

#### Child Node
- The node which is the immediate successor of a node.

#### Ancestor
- Any predecessor nodes on the path of the root to that node.

#### Descendant
- Any successor node on the path from the leaf node to that node.

#### Subtree
- Any node of the tree along with its descendant.

# Types of Tree with the Number of Children

<div align="center">
  <img src="https://github.com/TIBBOH17/CS/assets/121493257/d53ee658-dfd3-41a7-a20d-e38c93221000" width="50%", alt="">
</div>

#### Binary Tree
- Each node can have a maximum of two children linked to it.

#### Tenary Tree
- Each node has at most three child nodes.

#### N-ary Tree (Generic Tree)
- Each node is a data structure that consists of records and a list of references to its children.
 
# Types of Tree with the Nodes' Values
#### Binary Search Tree
- Shares similarities with a binary tree.
- The value of the left child in a binary search tree is always smaller than that of the parent node, and the value of the right child is larger than that of the parent node.
 
<div align="center">
    <img src="https://scaler.com/topics/images/the-binary-search-tree.webp", width="50%", alt="">
</div>

#### AVL Tree
- A self-balancing binary search tree.
- The balancing factor values vary between -1, 0, and 1.
    - If the right subtree is one level higher than the left subtree of a node, then the balancing factor value of that node is -1.
    - If both, the left and right subtrees are at the same level, the balancing factor value is given as 0.
    - If the left subtree is one level higher than the right subtree then the balancing factor is 1.

<div align="center">
    <img src="https://scaler.com/topics/images/the-avl-tree.webp", width="50%", alt="">
</div>
