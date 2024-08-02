## Create Binary tree


```javascript
 //One node in binary tree contains 3 component
      //root node, left child , right child
      class TreeNode {
        constructor(data) {
          this.data = data;
          this.left = null;
          this.right = null;
        }
      }

      //Create three node root node, left child , right child
      let binaryTree = new TreeNode("Drinks");
      let leftChild = new TreeNode("Cold");
      let rightChild = new TreeNode("Hot");

      //connect node to left and right child
      binaryTree.left = leftChild;
      binaryTree.right = rightChild;

      console.log(binaryTree);
```
Output :- 

<img src="images/binaryTree1.png" />


## PreOrder Traversal


```javascript
 //One node in binary tree contains 3 component
      //root node, left child , right child
      class TreeNode {
        constructor(data) {
          this.data = data;
          this.left = null;
          this.right = null;
        }
      }

      //Create three node root node, left child , right child
      let binaryTree = new TreeNode("Drinks");
      let leftChild = new TreeNode("Cold");
      let rightChild = new TreeNode("Hot");

      //connect node to left and right child
      binaryTree.left = leftChild;
      binaryTree.right = rightChild;

      //preorderTraversal
      function preOrderTraversal(rootNode) {
        if (rootNode === null) {
          return;
        }
        console.log(rootNode.data);
        preOrderTraversal(rootNode.left);
        preOrderTraversal(rootNode.right);
      }
      preOrderTraversal(binaryTree);
```

Output:-
Drinks
Cold
Hot










