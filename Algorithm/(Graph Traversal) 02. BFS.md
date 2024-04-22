# BFS
- Breadth-First Search
- An algorithm that starts from the start node of the graph and searches by first visiting nodes that are closer to the start node.

# Features of BFS
- Searching all the nodes.
- FIFO Searching
- Queue
- O(V+E) (V: number of nodes, E: number of edges)
 
# Implementing Process
- Represent the graph as an adjacency list.
```python
graph = {
    1: [2, 3],
    2: [5, 6],
    3: [4],
    4: [6],
    5: [],
    6: []
}
```
- Determine the starting node, and initialize the data structure to be used.
```python
from collections import deque

queue = deque()
queue.appendleft(start)
```
- Create a list of visited nodes.
```python
visited = []
```
- Pop a node from the queue and inserts adjacent nodes back into the stack if the popped node is not visited, and update the list of visited nodes.
```python
node = queue.pop()
if not node in visited:
    visited.append(node)
    for next_vode in graph[node]:
        queue.appendleft(next_node)
```
- Repeat until there are no values ​​on the queue.

# Implementation of Algorithm
```python
from collections import deque

def BFS(graph, start):
    queue = deque()
    queue.appendleft(start)
    visited = []
    
    while queue:
        node = queue.pop()
        if not node in visited:
            visited.append(node)
            for next_node in graph[node]:
                queue.appendleft(next_node)
    
    return visited
```
