# Graph
- A non-linear data structure.
- A collection of nodes connected by edges.

# Concepts of Graph

#### Vertices (Nodes)
- The fundamental units of the graph.
- Can be labeled or unlabeled.

#### Edges
- Connections between two nodes in the graph.
- Can be directed (having a direction) or undirected.
- Can be labeled or unlabeled.

# Types of Graph

#### Undirected Graph
- A graph in which edges do not have any direction.

#### Directed Graph (Digraph)
- A graph in which each edge has a direction.

#### Weighted Graph
- A graph in which each edge has an associated weight.

#### Cyclic Graph
- A graph that contains at least one cycle.

#### Acyclic Graph
- A graph that contains no cycles.

#### Connected Graph
- A graph in which there is a path between every pair of vertices.

#### Disconnected Graph
- A graph in which at least one pair of vertices is not connected by a path.

#### Complete Graph
- A graph in which every pair of vertices is connected by a unique edge.

# Representations of Graph

#### Edge List
- Represents the graph with respect to edges.
- Typically stored as a list of pairs (or triplets if weighted) of vertices.

#### Adjacency Matrix
- A 2D matrix where rows and columns represent vertices.
- Each entry in the matrix represents the presence (and possibly the weight) of an edge between the vertices.

#### Adjacency List
- A collection of lists or arrays.
- Each list corresponds to a vertex and contains the vertices adjacent to it.
