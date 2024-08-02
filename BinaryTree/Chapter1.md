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

<img src="images/btree.png" />


## PreOrder Traversal















