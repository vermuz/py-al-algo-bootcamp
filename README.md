# py-al-algo-bootcamp

### Table of Contents
- [Python Notes](#python-notes)
  - [Pythonic Swap](#pythonic-swap)
  - [Different Types of Sort](#different-types-of-sort)
  - [Python Bitwise](#python-bitwise)
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

#### Bubble Sort Omega(n)
Compares adjacent items and exchanges them if they are out of order.
#### Selection Sort Omega(n^2)
Improves on Bubble Sort by making one exchange for every pass through list. It looks for largest as it makes a pass
and after completing pass, it puts it in its proper place.
#### Insertion Sort Omega(n)
Always maintains a sorted sublist in lower positions of the list. Each new item is inserted into sublist such that the sorted
sublist is on item longer
#### Shell Sort Omega(nlogn)
Improves upon insertion sort by breaking original list into a number of smaller sublists each of which is sorted by
Insertion sort. It uses gap to construct sublist of certain length, at the end whatever is left also has its own Insertion
sort.
#### Merge Sort Omega(nlogn)
Divide and conquer algorithm. It continually splits a list in half
```
1 2 3 4 5
 123 45
```
I list has more than one items, we split the list and invoke merge sort on both halves. Finally, take sorted sublists and merge them into a complete list.
#### Quick Sort Omega(nlogn)
Divide and conquer algorithm. It has the same advantage as merge sort without extra memory. It can be done in place.
Selects a value called pivot, first or last value. Pivot assists in splitting the list. Elements smaller than pivot
in left of array (unsorted). Elements larger than pivot in right of array (unsorted). Partitioning locates position markers

### Python Bitwise

```
x = 2 -> 10 [0000 1010]
y = 4 -> 4 [0000 0100]
x = 0000 1010 = 10
y = 0000 0100 = 4
```

#### Bitwise AND

```
x & y

0000 1010
0000 0100
----------
0000 0000
```

#### Bitwise OR

```
x | y

0000 1010
0000 0100
---------
0000 1110
```

#### Bitwise NOT

```
0000 1010 -> 1111 0101 (-11)
```

#### Bitwise XOR

If values are different, result is 1

```
x ^ y 

0000 1010
0000 0100
----------
0000 1110 
```

#### Bitwise Right Shift

```
x = 0000 1010
x >> 2 = 0000 0010
```

#### Bitwise Left Shift

```
x = 0000 1010
x << 2 = 0010 1000
```

#### Check Parity
```
def parity(x):
    """
    An even number has parity 0 because the remainder after dividing by 2 is 0 , 
    while an odd number has parity 1 because the remainder after dividing by 2 is 1
    """
    result = 0
    while x:
        result ^= x & 1
        x >>= 1
    return result
```
