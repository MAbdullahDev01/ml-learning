# NumPy

## Getting Started

1. Install numpy via pip

```bash
pip install numpy
```

2. Check if numpy is working properly. The command should output the version you have currently installed.

  ```python
  import numpy as np
  print(np.__version__)
  ```

## Why use NumPy

- Written in C which makes it faster compared to traditional python code
- Allows vectorise operations on NumPy arrays

## Creating a 1D array using NumPy

```python
array = np.array([1, 2, 3, 4, 5])
print(array)
```

## Working with vectorise operations

```python
array = np.array([1, 2, 3, 4, 5])
array *= 2
print(array)
```

## Creating multidimensional arrays using NumPy

1. Zero dimension array
  ```python
  zero_dimensional_array = np.array("A")
  print(zero_dimensional_array.ndim) # output 0
  ```

2. One dimension array
   ```python
  one_dimensional_array = np.array(["A", "B", "C"])
  print(one_dimensional_array.ndim) # output 1
  ```

3. Two dimension array
  ```python
  two_dimensional_array = np.array([["A", "B", "C"],
                                  ["D", "E", "F"],
                                  ["G", "H", "I"]])
  print(two_dimensional_array.ndim) # output 2
  ```

4. Three dimension array
  ```python
  three_dimensional_array = np.array([[["A", "B", "C"], ["D", "E", "F"], ["G", "H", "I"]],
                                      [["J", "K", "L"], ["M", "N", "O"], ["P", "Q", "R"]],
                                      [["S", "T", "U"], ["V", "W", "X"], ["Y", "Z", "_"]]])
  print(three_dimensional_array.ndim) # output 3
  ```

## NumPy array.shape

- Returns a tuple with the depth of the array, rows in the array and the columns
```python
print(zero_dimensional_array.shape)     # Returns ()
print(one_dimensional_array.shape)      # Returns (3,)
print(two_dimensional_array.shape)      # Returns (3, 3)
print(three_dimensional_array.shape)    # Returns (3, 3, 3)
```

## Multidimensional Indexing

- Returns the stored value at the given index
```python
print(three_dimensional_array[2,1,2]) # output X
```

## Slicing

- Slicing is done using this generic way array[start:end:step]
```python
array = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12], [13, 14, 15, 16]])  # 2D array with shape (4, 4)
print(array[0:3:2]) # Output: [[ 1 2 3 4] [ 9 10 11 12]]
```

- End is exclusive in slicing so for arrays 0 to 2 you need to put end as 3

- Slicing and indexing:
```python
array = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12], [13, 14, 15, 16]])  # 2D array with shape (4, 4)
print(array[0:3:2, 0:4:2]) # Output: [[ 1 3] [ 9 11]]