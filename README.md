# py-al-algo-bootcamp

### Table of Contents
- [Python Notes](#python-notes)
  - [Pythonic Swap](#pythonic-swap)
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
