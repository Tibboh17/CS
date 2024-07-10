# Sorting Algorithm
- An algorithm that puts elements of a list into a specific order based on a comparison operator.

# Stability

#### Stable Sort
- Maintains the relative order of items with equal sort keys.
- Examples: Bubble Sort, Insertion Sort, Merge Sort.

#### Unstable Sort
- Does not maintain the relative order of items with equal sort keys.
- Examples: Selection Sort, Quick Sort.

# In-Place
#### In-Place Algorithm
- Sorts the input array in place, without using additional memory (strict definition).
- May use a small amount of extra space (broad definition).
- Examples: Bubble Sort, Selection Sort, Insertion Sort, Quick Sort (by broad definition).

#### Not In-Place Algorithm
- Requires additional memory for sorting.
- Examples: Merge Sort, Heap Sort.

# Types of Sorting Algorithm
#### Bubble Sort
- Compares adjacent elements and swaps them if they are in the wrong order.
- **Time Complexity**: O(N^2)
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        for j in range(n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr
```

#### Selection Sort
- Repeatedly finds the minimum element from the unsorted part and moves it to the sorted part.
- **Time Complexity**: `O(N^2)`
```python
def selection_sort(arr):
    for i in range(len(arr) - 1):
        min_idx = i
        for j in range(i + 1, len(arr)):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
    return arr
```

#### Insertion Sort
- Builds the sorted array one item at a time by inserting elements in their correct position.
- **Time Complexity**: `O(N^2)`
```python
def insertion_sort(arr):
    for end in range(1, len(arr)):
        i = end
        while i > 0 and arr[i - 1] > arr[i]:
            arr[i - 1], arr[i] = arr[i], arr[i - 1]
            arr -= 1
    return arr
```

#### Quick Sort
- Selects a pivot and partitions the array around the pivot, then recursively sorts the partitions.
- **Time Complexity**: `O(NlogN)` on average, `O(N^2)` in the worst case
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr

    pivot, tail = arr[0], arr[1]
    left_side = [x for x in tail if x <= pivot]
    right_side = [x for x in tail if x > pivot]
    
    return quick_sort(left_side) + [pivot] + quick_sort(right_side)
```

#### Merge Sort
- Divides the array into halves, recursively sprts them, and then merges the sorted halves.
- **Time Complexity**: `O(NlogN)`
```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    sorted_arr = []
    i, j = 0, 0
    
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            sorted_arr.append(left[i])
            i += 1
        else:
            sorted_arr.append(right[j])
            j += 1
    
    while i < len(left):
        sorted_arr.append(left[i])
        i += 1
        
    while j < len(right):
        sorted_arr.append(right[j])
        j += 1
        
    return sorted_arr
```

# Applications of Sorting Algorithm
#### Searching
- Sorting helps in efficiently searching elements using algorithms like binary search.

#### Data Organization
- Helps in arranging data for better readability and organization.

#### Algorithms
- Many algorithms like graph algorithms rely on sorting as a subroutine.

#### Databases
- Sorting is crucial for query optimization and efficient data retrieval.

#### Machine Learning
- Data preprocessing often involves sorting to organize and analyze data.
