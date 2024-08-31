## Drawbacks of Linear Queue Implemented by Array

1. Wasted Space: After several dequeue operations, the front of the queue moves forward, leaving unused space at the beginning of the array. This space cannot be reused, leading to inefficient memory utilization.
2. Fixed Size: The size of the array is fixed at the time of creation. If the queue becomes full, you cannot add more elements even if there is unused space at the beginning.
3. Overflow Condition: Even if there is space available at the beginning of the array, the queue can still overflow if the rear reaches the end of the array.

## How Circular Queue Overcomes These Drawbacks

1. Efficient Memory Utilization: In a circular queue, the rear pointer wraps around to the beginning of the array when it reaches the end. This allows the queue to reuse the space left by dequeue operations, making better use of available memory.
2. No Overflow Until Full: The circular queue only overflows when all positions in the array are occupied, ensuring that all available space is utilized before declaring the queue full.
3. Dynamic Front and Rear Management: The front and rear pointers move in a circular manner, allowing continuous insertion and deletion of elements without the need for shifting elements or wasting space


Note :- Think it as a clock 🕒 where after 12 it goes to the 1 , by clearing 1 to 12 numbers , and again run  a loop.

## create a linear queue with fix size.

### All the ways to create a fix array in javascript

```javascript
//one - with empty items
let arr = new Array(5);
console.log(arr.length); // 5
console.log(arr); // [ <5 empty items> ]

//two - fith filled items
let arr = new Array(5).fill(0);
console.log(arr.length); // 5
console.log(arr); // [0, 0, 0, 0, 0]

//three pass index number as value
let arr = Array.from({ length: 5 }, (_, i) => i);
console.log(arr.length); // 5
console.log(arr); // [0, 1, 2, 3, 4]

//fouth - with spread operator
let arr = [...Array(5)].map(() => 0);
console.log(arr.length); // 5
console.log(arr); // [0, 0, 0, 0, 0]

//it will create a array of size 5 and map method will loop the array and create a new array with value 0

```

### queue code with fix size

```javascript
class Q {
  constructor(size) {
    this.size = size;
    this.queue = new Array(size);
    //rear is at right and work with enqueue "add from right"
    this.rear = -1;
    //front is at left and work with dequeue 'remove from left'
    this.front = -1;
  }
  enqueue(data) {
    if (this.front === -1) this.front = 0;
    // Check if the queue is full
    //one element in the queue means "this.rear == 0"
    //n element = "this.rear == n-1"
    //3 element = "this.rear == 3-1=2" this.rear is at index 2 means its full
    //this.rear === 2 "means full"
    //compare with "this.size" size is 3
    //we should stop when both are equal
    //2<2 ==== run when it rear is -1 , 0 , 1
    //we are updating the rear inside
    //outside its value start from -1
    //1<2 "if size is 3, subtract to 1 and it will become 2 and run the block until 1< 2, stop if it become 2==2
    if (this.rear < this.size - 1) {
      this.rear++;
      this.queue[this.rear] = data;
      return this.queue;
    } else {
      return "queue is full";
    }
  }
}

let qq = new Q(3);
console.log(qq.enqueue(10));
console.log(qq.enqueue(10));
console.log(qq.enqueue(10));
console.log(qq.enqueue(10));
console.log(qq.enqueue(10));

```

























