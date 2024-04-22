# Binary Search
- An algorithm to find the desired value when data is sorted.
- Compare the median value of the data with the target value you want to find and explore by reducing the size of the data by half.

# Features of Binary Search
- Searching the target data.
- Target reduction method through median comparison.
- O(logN)

# Implementing Process
- Select the median of the current data
```python
start = 0
end = len(data) - 1
mid = (start + end) // 2
median = data[mid]
```
- If median < target, take the right side of the data.
```python
if median < target:
    start = mid + 1
```
- If median > target, take the right side of the data.
```python        
elif median > target:
    end = mid - 1
```
- Repeat this process until median == target.
```python
else:
    return median
```

# Implemetation of Algorithm
```python
def BinarySearch(data, target):
    start = 0
    end = len(data) - 1
    data.sort()

    while start <= end:        
        mid = (start + end) // 2
        if data[mid] == target:
            return mid
        elif data[mid] < target:
            start = mid + 1 
        else:
            end = mid - 1

    return -1
```
