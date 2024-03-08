# DFS
- Depth-First Search
- An algorithm that starts from the start node of the graph, determines one branch to explore, completes the search to the maximum depth, and then moves to the other branch and performs the search again.
- Function
  - Searching all the nodes.
- Characteristic
  - Recursive function
  - Stack
- Time Complexity
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
stack = [start]
```
- Create a list of visited nodes.
```python
visited = []
```
- Pop a node from the stack and inserts adjacent nodes back into the stack if the popped node is not visited, and update the list of visited nodes.
```python
node = stack.pop()
if node not in visited:
    visited.append(node)
    for next_node in graph[node]:
        stack.append(next_node)
```
- Repeat until there are no values ​​on the stack.

# Implementation of Algorithm
```python
def DFS(graph, start):
    stack = [start]
    visited = []
    
    while stack:
        node = stack.pop()
        if node not in visited:
            visited.append(node)
            for next_node in graph[node]:
                stack.append(next_node)
    
    return visited
```
