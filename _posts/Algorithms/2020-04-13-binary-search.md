---
layout: post
title: "Binary Search"
date: 2020-04-13 16:12:40
tags: [algorithms, python]
---


Binary search searches for the element from **sorted array**.

First, compare the target value with the middle element from the sorted array. If the target value is bigger than the middle element, eliminate the elements on the left of the array. *(Since the array is sorted, it would eliminate elements that are smaller than the middle element.)*

Repeat the process with the remaining elements. Each process eliminates half of the remaining array. So, in the worst case, it would take log n steps -- **O(log *n*)**.


```python
def binary_search (list, item):
  low = 0
  high = len(list)-1

  while low <= high:
    mid = (low + high)//2
    guess = list[mid]

    if guess == item:
      return mid
    if guess > item:
      high = mid - 1
    else:
      low = mid + 1
  return None


my_list = [4, 6, 8, 20, 39, 60, 67, 90, 104, 204]

print(binary_search(my_list, 20))
```
