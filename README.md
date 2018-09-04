# py-al-algo-bootcamp

### Table of Contents
- [Python Notes](#python-notes)
  - [Pythonic Swap](#pythonic-swap)
  - [Different Types of Sort](#different-types-of-sort)
- [Data Structures and Algorithms](#data-structures-and-algorithms)

### Python Notes

#### Pythonic Swap

Python Swap is different from traditional Swap

```python
if a[i] > a[i+1]:
  temp = a[i]
  a[i] = a[i+1]
  a[i+1] = temp
```

would instead be written as,
```python
if a[i] > a[i+1]:
  a[i], a[i+1] = a[i+1], a[i]
```

### Data Structures and Algorithms

#### Different Types of Sort

- Bubble Sort Omega(n)
Compares adjacent items and exchanges them if they are out of order.
- Selection Sort Omega(n^2)
Improves on Bubble Sort by making one exchange for every pass through list. It looks for largest as it makes a pass
and after completing pass, it puts it in its proper place.
- Insertion Sort Omega(n)
Always maintains a sorted sublist in lower positions of the list. Each new item is inserted into sublist such that the sorted
sublist is on item longer
- Shell Sort Omega(nlogn)
Improves upon insertion sort by breaking original list into a number of smaller sublists each of which is sorted by
Insertion sort. It uses gap to construct sublist of certain length, at the end whatever is left also has its own Insertion
sort.
- Merge Sort Omega(nlogn)
Divide and conquer algorithm. It continually splits a list in half
```
1 2 3 4 5
 123 45
```
I list has more than one items, we split the list and invoke merge sort on both halves. Finally, take sorted sublists and merge them into a complete list.
- Quick Sort Omega(nlogn)
Divide and conquer algorithm. It has the same advantage as merge sort without extra memory. It can be done in place.
Selects a value called pivot, first or last value. Pivot assists in splitting the list. Elements smaller than pivot
in left of array (unsorted). Elements larger than pivot in right of array (unsorted). Partitioning locates position markers
