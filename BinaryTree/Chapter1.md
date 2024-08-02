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


## PreOrder Traversal of Binary Tree


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



## InOrder Traversal of Binary Tree


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
      let chai = new TreeNode("chai");
      let coffee = new TreeNode("coffee");

      let cola = new TreeNode("cola");
      let fenta = new TreeNode("fenta");

      //connect node to left and right child
      //drink -- cold ---hot
      binaryTree.left = leftChild;
      binaryTree.right = rightChild;

      //connect hot to left and right child
      //hot  -- chai -- coffee
      rightChild.left = chai;
      rightChild.right = coffee;

      //connect cold to left and right child
      //cold  -- cola -- fenta
      leftChild.left = cola;
      leftChild.right = fenta;

      console.log(binaryTree);

      //inOrdertraversal
      function inOrderTraversal(rootNode) {
        if (rootNode === null) {
          return;
        }
        inOrderTraversal(rootNode.left);
        console.log(rootNode.data);
        inOrderTraversal(rootNode.right);
      }

      inOrderTraversal(binaryTree);
```


Output:- 

<img src="images/binaryTree2.png" />



## PostOrder Traversal of Binary Tree


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
      let chai = new TreeNode("chai");
      let coffee = new TreeNode("coffee");

      let cola = new TreeNode("cola");
      let fenta = new TreeNode("fenta");

      //connect node to left and right child
      //drink -- cold ---hot
      binaryTree.left = leftChild;
      binaryTree.right = rightChild;

      //connect hot to left and right child
      //hot  -- chai -- coffee
      rightChild.left = chai;
      rightChild.right = coffee;

      //connect cold to left and right child
      //cold  -- cola -- fenta
      leftChild.left = cola;
      leftChild.right = fenta;

      console.log(binaryTree);

      //postOrderTraversal
      function postOrderTraversal(rootNode) {
        if (rootNode === null) {
          return;
        }
        postOrderTraversal(rootNode.left);
        postOrderTraversal(rootNode.right);
        console.log(rootNode.data);
      }

      postOrderTraversal(binaryTree);
```



<img src="images/binaryTree3.png" />



















