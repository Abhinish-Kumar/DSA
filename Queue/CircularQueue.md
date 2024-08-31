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





























