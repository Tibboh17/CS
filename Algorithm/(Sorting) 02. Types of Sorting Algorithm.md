# Bubble Sort
- A method of comparing adjacent elements, performing swap operations, and sorting
- Time Complexity: O(N^2)
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n-1):
        for j in range(n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr
```

# Selection Sort
- A method of sorting by finding the largest or smallest data in the target and repeating the selection.
- Time Complexity: O(N^2)
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

# Insertion Sort
- A method of sorting by selecting an object, finding the appropriate location for the selected data in the sorted area, and inserting it.
- Time Complexity: O(N^2)
```python
def insertion_sort(arr):
    for end in range(1, len(arr)):
        i = end
        while i > 0 and arr[i-1] > arr[i]:
            arr[i-1], arr[i] = arr[i], arr[i-1]
            i -= 1
    return arr
```

# Quick Sort
- A method of selecting the pivot value and sorting based on that value.
- Time Complexity: O(nlogn), O(N^2) (Depends on the choice of pivot value.)
```python
def quick_sort(arr):
    if len(arr) <= 1: 
        return arr
    
    pivot, tail = arr[0], arr[1:]
    leftSide = [x for x in tail if x <= pivot]
    rightSide = [x for x in tail if x > pivot]
    
    return quick_sort(leftSide) + [pivot] + quick_sort(rightSide)
```

# Merge Sort
- A method of sorting the whole by efficiently merging already sorted subsets.
- Time Complexity: O(nlogn)
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

# Counting Sort
- A method of sorting the elements of an array by counting the number of occurrences of each unique element in the array.
- Works well when there is a limited range of input values.
- Time Complexity: O(n+m) (n: the size of input array, m: the size of count array)
```python
def counting_sort(arr):
    max_num = max(arr)
    count_arr = [0 for _ in range(max_num+1)]
    sorted_arr = [0 for _ in range(len(arr))]
    
    for i in arr:
        count_arr[i] = arr.count(i)
    
    for i in range(1, max_num+1):
        count_arr[i] += count_arr[i-1]
        
    j = len(arr) - 1
    while j >= 0:
        sorted_arr[count_arr[arr[j]]-1] = arr[j]
        count_arr[arr[j]] -= 1
        j -= 1
    
    return sorted_arr
```
