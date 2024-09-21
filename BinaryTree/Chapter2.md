# Array implementation of Binary tree

## Create a Binary tree

```javascript
class BinaryTree {
        constructor(size) {
          this.array = [];
          this.maxSize = size;
          this.lastUsedIndex = 0;
        }
      }
      let newTree = new BinaryTree(5);
      console.log(newTree);
```

## Insert a Node in BT

```javascript
class BinaryTree {
        constructor(size) {
          this.array = [];
          this.maxSize = size;
          this.lastUsedIndex = 0;
        }
        insertNode(item) {
          if (this.lastUsedIndex + 1 >= this.maxSize) {
            return "Tree is full";
          } else {
            this.array[this.lastUsedIndex + 1] = item;
            this.lastUsedIndex++;
          }
        }
      }
      let newTree = new BinaryTree(5);
      console.log(newTree);
      newTree.insertNode("Drinks");
      newTree.insertNode("Hot");
      newTree.insertNode("Cold");
      newTree.insertNode("Chai");
      newTree.insertNode("Cap");
      newTree.insertNode("wind");
      newTree.insertNode("fanta");

      console.log(newTree);
```










