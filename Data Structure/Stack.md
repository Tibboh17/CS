# Stack
- A stack is a linear data structure that follows a specific order for operations.
- LIFO (Last In, First Out): The last element added to the stack will be the first one to be removed.

# Types of Stack
#### Fixed Size Stack
- A fixed size stack has a pre-defined capacity and cannot grow or shrink dynamically.
- Typically implemented using arrays.
- Efficient in terms of access time, but limited by its fixed size which may lead to overflow.

#### Dynamic Size Stack
- A dynamic size stack can grow or shrink dynamically as needed.
- Usually implemented using a linked list or dynamic arrays (like Python lists).
- More flexible as it can adjust its size, but might incur overhead for dynamic resizing.

# Operations of Stack
#### Push
- Add an element to the top of the stack, increasing its size by one.
- **Time complexity:** O(1)

#### Pop
- Remove the element from the top of the stack, decreasing its size by one, and return the removed element.
- **Time complexity:** O(1)

#### Peek (or Top)
- Retrieve the top element of the stack without removing it, allowing a look at the value without modifying the stack.
- **Time complexity:** O(1)

#### isFull
- Check if the stack is full (only applicable for fixed size stacks).
- **Time complexity:** O(1)

#### isEmpty
- Check if the stack is empty.
- **Time complexity:** O(1)

#### Size
- Return the number of elements currently in the stack.
- **Time complexity:** O(1)

# Applications of Stack
#### Function Call
- Stacks are used in function call management, storing return addresses, local variables, and function parameters. This allows the program to return to the correct location after a function completes.
  
#### Recursion
- In recursive function calls, stacks store the local variables and return addresses. This enables the program to keep track of the current state of the recursion, ensuring each call returns correctly.

#### Expression Evaluation
- Stacks are used to evaluate expressions, especially those in postfix notation (Reverse Polish Notation). The stack aids in processing operators and operands in the correct order.

#### Syntax Parsing
- Stacks help in syntax parsing, used in compilers and interpreters to check the correctness of expressions, balance parentheses, and manage nested structures.

#### Memory Management
- Stacks are utilized in memory management for allocating and deallocating memory in a LIFO manner. This is particularly common in runtime memory management for programming languages.

# Additional Details
#### Underflow and Overflow
- In a fixed size stack, attempting to pop from an empty stack causes underflow, and trying to push into a full stack causes overflow.

#### Linked List Implementation
- In a dynamic stack implemented using a linked list, each node contains the data and a reference to the next node. The top of the stack is represented by the head of the linked list.

#### Dynamic Array Implementation
- In a dynamic stack implemented using a dynamic array, the array resizes itself (usually doubling in size) when the capacity is reached, ensuring amortized O(1) time complexity for push operations.
