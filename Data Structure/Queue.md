# Queue
- A queue is a linear data structure that follows a specific order for operations.
- FIFO (First In, First Out): The first element added to the queue will be the first one to be removed.

# Types of Queue
#### Simple Queue
- A simple queue has a fixed size and elements are added at the rear and removed from the front.
- Typically implemented using arrays.

#### Circular Queue
- A circular queue is a queue in which the last position is connected back to the first position to make a circle.
- This allows efficient use of memory by reusing empty spaces created by dequeuing elements.

#### Priority Queue
- A priority queue is a type of queue in which each element is associated with a priority.
- Elements are dequeued based on their priority rather than their order in the queue.

#### Double-ended Queue (Deque)
- A double-ended queue allows insertion and deletion of elements from both the front and the rear.

# Operations of Queue
#### Enqueue
- Add an element to the rear of the queue, increasing its size by one.
- **Time complexity:** O(1)

#### Dequeue
- Remove the element from the front of the queue, decreasing its size by one, and return the removed element.
- **Time complexity:** O(1)

#### Front (or Peek)
- Retrieve the front element of the queue without removing it, allowing a look at the value without modifying the queue.
- **Time complexity:** O(1)

#### isFull
- Check if the queue is full (only applicable for fixed size queues).
- **Time complexity:** O(1)

#### isEmpty
- Check if the queue is empty.
- **Time complexity:** O(1)

#### Size
- Return the number of elements currently in the queue.
- **Time complexity:** O(1)

# Applications of Queue
#### CPU Scheduling
- Queues are used in operating systems for scheduling tasks. Processes are kept in the queue and scheduled for execution based on their order.

#### Disk Scheduling
- Queues manage the order in which disk I/O requests are processed, optimizing read/write operations.

#### Print Spooling
- Print jobs are queued and processed in the order they are received, allowing multiple print jobs to be managed efficiently.

#### Data Streaming
- Queues are used in data streaming to manage data packets and ensure they are processed in the correct order.

#### Breadth-First Search (BFS)
- In graph algorithms like BFS, queues are used to keep track of nodes to be explored, ensuring nodes are processed in the order they are discovered.

# Additional Details
#### Underflow and Overflow
- In a fixed size queue, attempting to dequeue from an empty queue causes underflow, and trying to enqueue into a full queue causes overflow.

#### Circular Queue Implementation
- Circular queues use a fixed-size array and two pointers (front and rear) to manage the elements, wrapping around the array when the end is reached.

#### Linked List Implementation
- In a dynamic queue implemented using a linked list, each node contains the data and a reference to the next node. The front of the queue is represented by the head of the linked list, and the rear is represented by the tail.
