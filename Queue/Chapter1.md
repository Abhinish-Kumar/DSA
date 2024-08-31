## Implement queue in javascript

```javascript
class Q {
  constructor() {
    this.queue = []; // Initialize an empty array to represent the queue
  }

  // Add an element to the end of the queue
  enqueue(element) {
    this.queue.push(element);
  }

  // Check if the queue is empty
  isEmpty() {
    return this.queue.length === 0;
  }

  // Remove and return the element at the front of the queue
  dequeue() {
    if (this.isEmpty()) {
      return "Queue is Empty"; // Return a message if the queue is empty
    }
    return this.queue.shift(); // Remove the first element and shift the rest
  }

  // Return the element at the front of the queue without removing it
  front() {
    if (this.isEmpty()) {
      return "No element in the queue"; // Return a message if the queue is empty
    }
    return this.queue[0]; // Return the first element of the queue
  }

  // Return the current size of the queue
  size() {
    return this.queue.length;
  }

  // Print all elements in the queue
  printQueue() {
    let queueElements = "";
    for (let i = 0; i < this.size(); i++) {
      queueElements += this.queue[i] + " , ";
    }
    console.log(queueElements); // Print the elements separated by commas
  }
}

// Create a new instance of the queue
let personQueue = new Q();
console.log(personQueue.isEmpty()); // Output: true, since the queue is empty
console.log(personQueue.front()); // Output: "No element in the queue", since it's empty

// Add elements to the queue
personQueue.enqueue(666);
personQueue.enqueue(567);
personQueue.enqueue(856);

// Print the current state of the queue
personQueue.printQueue(); // Output: 666 , 567 , 856 ,
console.log(personQueue.size()); // Output: 3, since three elements are in the queue

// Remove elements from the front of the queue
personQueue.dequeue();
personQueue.dequeue();
console.log(personQueue.front()); // Output: 856, the next element at the front

// Print the current state of the queue after dequeuing
personQueue.printQueue(); // Output: 856 ,

// Print the current size of the queue
console.log(personQueue.size()); // Output: 1, since one element remains

// Check if the queue is empty
console.log(personQueue.isEmpty()); // Output: false, since there's still an element

```

| **Method**        | **Time Complexity** | **Space Complexity** |
|-------------------|---------------------|----------------------|
| `enqueue(element)`| `O(1)`              | `O(1)`               |
| `isEmpty()`       | `O(1)`              | `O(1)`               |
| `dequeue()`       | `O(n)`              | `O(1)`               |
| `front()`         | `O(1)`              | `O(1)`               |
| `size()`          | `O(1)`              | `O(1)`               |
| `printQueue()`    | `O(n)`              | `O(n)`               |

### **Overall Space Complexity of the `Q` class:** `O(n)`


Note:- Problem of this array is that dequeue is taking O(n) time because of the shifting of array elements , by deleting elements from index 0.




## Example 2


```javascript

class Q {
  constructor() {
    this.queue = [];
    this.rear = -1;
    this.front = -1;
  }
  enqueue(data) {
    //remove from front left , starting of queue
    if (this.front === -1) this.front = 0;
    //if rear is -1 increment to make it 0 a valid index to inset data
    this.rear++;
    this.queue[this.rear] = data;
    return this.queue;
  }
  dequeue() {
    this.queue[this.front] = null;
    this.front++;
    return this.queue;
  }
  printQueue() {
    //slice , start fron given index till end (not included)
    //avoid using this O(n)time complexity
    let ququeData = this.queue.slice(this.front, this.rear + 1);
    console.log(ququeData);
  }
}

let q = new Q();
q.enqueue(10);
q.enqueue(20);
q.enqueue(30);
q.enqueue(40);
q.dequeue();
q.dequeue();
q.enqueue(50);
q.enqueue(60);
q.enqueue(70);
q.enqueue(80);
q.enqueue(50);
q.enqueue(60);
q.enqueue(70);
q.enqueue(80);

console.log(q.enqueue(50));
q.printQueue();

```

| Operation | Time Complexity | Space Complexity |
|-----------|-----------------|------------------|
| enqueue   | O(1)            | O(1)             |
| dequeue   | O(1)            | O(1)             |






