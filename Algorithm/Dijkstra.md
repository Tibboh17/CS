# Dijkstra
- An algorithm for finding the shortest distance in a graph.
- **Function**
  - Finding the shortest distance between the starting node and all nodes.
- **Feature**
  - Edges are all positive.
- **Time Complexity**
  - O(ElogV) (V: number of nodes, E: number of edges)

# Implementing Process
- Represent the graph as an adjacency list.
```python
graph = {
    0: [(1, 1)],
    1: [(0, 1), (2, 2), (3, 3)],
    2: [(1, 2), (3, 1), (4, 5)],
    3: [(1, 3), (2, 1), (4, 1)],
    4: [(2, 5), (3, 1)]
}
```
- Create a list of distances and initialize all node distances as infinite.
```python
distances = {node: float('infinity') for node in graph}
distances[start] = 0
```
- Create a list of visited nodes set to False for each node. 
```python
visited = {node: False for node in graph}
```
- Create a priority queue to hold the vertex with the smallest distance and put the priority '0' for the node 'start'.
```python
from queue import PriorityQueue

priority_queue = PriorityQueue()
priority_queue.put((0, start))
```
- Check if the current node is visited. If the node has been visited skip it, otherwise set it as visited i.e True.
```python
current_distance, current_node = priority_queue.get()

if visited[current_node]:
    continue
visited[current_node] = True
```
- Update the distance for each neighboring node of that visited node, by calculating if the sum of the distance of the current node from the source and weight of an edge between the current node and the neighboring node is less than the distance value of the neighboring vertex.
```python
for next_node, weight in graph[current_node]:
    if distance[current_node] + weight < distance[next_node]:
        distance[next_node] = distance[current_node] + weight
        priority_queue.put((distance[next_node], next_node))
```

# Implementation of Algorithm
```python
from queue import PriorityQueue

def Dijkstra(graph, start):
    distances = {vertex: float('infinity') for vertex in graph}
    distances[start] = 0
    
    visited = {vertex: False for vertex in graph}
    
    priority_queue = PriorityQueue()
    priority_queue.put((0, start))
    
    while priority_queue.qsize() > 0:
        current_distance, current_vertex = priority_queue.get()
        
        if visited[current_vertex]:
            continue
        visited[current_vertex] = True
        
        for next_vertex, weight in graph[current_vertex]:
            if distances[next_vertex] > distances[current_vertex] + weight:
                distances[next_vertex] = distances[current_vertex] + weight
                priority_queue.put((distances[next_vertex], next_vertex))
                
    print(distances)
```
