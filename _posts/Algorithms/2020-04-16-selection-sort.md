---
layout: post
title: "Selection Sort"
date: 2020-04-16 18:57:00
tags: [algorithms, python]
---

Selection sort starts off with comparing the first element with the remaining elements. After the first iteration, if the smallest value is found, the element at index 0 and the smallest element will be swapped. This process will be repeated until the second to the last value. Just like first iteration, during second iteration, the rest of the elements, except the first one, will be inspected to find the next smallest value. When the iteration finishes, the entire array will be sorted in ascending order.

The first iteration takes O(n) time since it touches every elements in the list, and it has to be done n times. Therefore selection sort takes **O (n<sup>2</sup>)**.

### first iteration (i = 0)

| | | | | |
|-|-|-|-|-|
|10|4|6|2|5|

*start iteration assuming minimum is at index i*
- min = 0 *and* j = 1, arr[min] = 10 *and* arr[j] = 4 *are being compared and the minimum is index 1*

- min = 1 *and* j = 2, arr[min] = 4 *and* arr[j] = 6 *so minimum is still at index 1.*

- min = 1 *and* j = 3, arr[min] = 4 *and* arr[j] = 2. *Now minimum is index j, 3.*

- min = 3 *and* j = 4, arr[min] = 2 *and* arr[j] = 5. *Minimum is at index 3.*

Swap index i and index 3
2|4|6|10|5


### second iteration (i=1)

2|4|6|10|5

*start iteration assuming minimum is at index i*

- min = 1 *and* j = 2, arr[min] = 4 *and* arr[j] = 6 *smallest number is at index 1.*

- min = 1 *and* j = 3, arr[min] = 4 *and* arr[j] = 10 *smallest number is at index 1.*

- min = 1 *and* j = 4, arr[min] = 4 *and* arr[j] = 5 *smallest number is at index 1.*

No swapping for second iteration.
2|4|6|10|5


### third iteration (i=2)

2|4|6|10|5


*start iteration assuming minimum is at index i*

- min = 2 *and* j = 3, arr[min] = 6 *and* arr[j] = 10 *smallest number is at index 2.*

- min = 2 *and* j = 4, arr[min] = 6 *and* arr[j] = 5 *smallest number is at index 4.*

Swap index i and index j
2|4|5|10|6


### fourth iteration (i=3)

2|4|5|10|6


*start iteration assuming minimum is at index i*

- min = 3 *and* j = 4, arr[min] = 10 *and* arr[j] = 6 *smallest number is at index 4.*

Swap index i and index j
2|4|5|6|10
