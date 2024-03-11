# Union-Find
- **Union**
    - An algorithm that merges disjoint sets to a single disjoint set.
- **Find**
    - An algorithm that finds a representative of a disjoint set.
 
# Implementing Process
- In initializing step, since there is no connection, the representaive of each node is itself.
```python
{'A': 'A', 'B': 'B', 'C': 'C', 'D': 'D', 'E': 'E', 'F': 'F'}
```
- If union('A', 'D'), then the representative of 'A', 'D' is 'A'.
```python
{'A': 'A', 'B': 'B', 'C': 'C', 'D': 'A', 'E': 'E', 'F': 'F'}
```
- If union('E', 'F'), then the representative of 'E', 'F' is 'E'.
```python
{'A': 'A', 'B': 'B', 'C': 'C', 'D': 'A', 'E': 'E', 'F': 'E'}
```
- If union('D', 'F'), then the result is different from previous steps because the union operation connects the representatives of each node.
```python
{'A': 'A', 'B': 'B', 'C': 'C', 'D': 'A', 'E': 'A', 'F': 'E'}
```
- Since the root nodes of 'D', 'F' are 'A', 'E' respectively and 'E' is not the representative itself, we have to find('F').
```python
{'A': 'A', 'B': 'B', 'C': 'C', 'D': 'A', 'E': 'A', 'F': 'A'}
```

# Implemetation of Algorithm
```python
arr = {'A': 'A', 'B': 'B', 'C': 'C', 'D': 'D', 'E': 'E', 'F': 'F'}

def find_parent(x):
    if arr[x] == x:
        return x
    else:
        arr[x] = find_parent(arr[x])
        return arr[x]

def union_parent(a, b):
    parent_a = find_parent(a)
    parent_b = find_parent(b)
    
    if parent_a != parent_b:
        if parent_a < parent_b:
            arr[parent_b] = parent_a
        else:
            arr[parent_a] = parent_b
```
