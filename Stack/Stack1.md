## Array implementation of Stack 

```js
class Stack {
        constructor(size = 10) {
          this.size = size;
          this.top = -1;
          this.array = new Array(size);
        }
        isEmpty() {
          return this.top === -1;
        }
        isFull() {
          return this.top === this.size - 1;
        }
        push(element) {
          if (this.isFull()) {
            console.log("Stact overflow");
          } else {
            this.top += 1;
            this.array[this.top] = element;
          }
        }
        pop() {
          if (this.isEmpty()) {
            console.log("Stack underflow");
          } else {
            let currentElement = this.array[this.top];
            this.top -= 1;
            return currentElement;
          }
        }

        peek() {
          return this.array[this.top];
        }
        //         display() {
        //           for (let i = 0; i < this.array.length; i++) {
        //             console.log(this.array[i]);
        //           }
        //         }
      }

      let s = new Stack();
      s.push(100);
      s.push(200);
      s.push(300);
      s.push(400);
      s.push(500);
      s.push(600);
      s.push(700);
      s.push(800);
      s.push(900);
      s.push(1000);
      console.log(s.array);
```
