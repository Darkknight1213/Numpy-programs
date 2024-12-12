# NumPy Programs

### 1. Create a vector with values from 0 to 20 and change the sign of the numbers in the range from 9 to 15.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

# Initializing an array with values from 0 to 20.
vector = np.arange(0, 21)
print(vector)

# Changing the sign of numbers in the range from 9 to 15.
vector[9:16] *= -1
print(vector)
```

```text
Output:
[ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20]
[ 0  1  2  3  4  5  6  7  8 -9 -10 -11 -12 -13 -14 -15 16 17 18 19 20]
```


### 2. Create a 10x10 matrix where the border elements are 1 and the inner elements are 0.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

mat = np.zeros((10, 10), dtype=int)
mat[0, :] = mat[-1, :] = mat[:, 0] = mat[:, -1] = 1

print(mat)
```

```text
Output:
[[1 1 1 1 1 1 1 1 1 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 0 0 0 0 0 0 0 0 1]
 [1 1 1 1 1 1 1 1 1 1]]
```

---

### 3. Create an array of 10 zeros, 10 ones, and 10 fives.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

zeros = np.zeros(10)
ones = np.ones(10)
fives = np.full(10, 5)

print(zeros)
print(ones)
print(fives)
```

```text
Output:
[0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
[1. 1. 1. 1. 1. 1. 1. 1. 1. 1.]
[5 5 5 5 5 5 5 5 5 5]
```

---

### 4. Add a vector to each row of a given matrix.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

mat = np.random.randint(0, 10, size=(3, 3))
vect = np.random.randint(0, 10, size=(1, 3))

added_matrix = mat + vect

print("Matrix:")
print(mat)
print("\nVector:")
print(vect)
print("\nMatrix + Vector:")
print(added_matrix)
```

```text
Output:
Matrix:
[[7 1 5]
 [6 4 0]
 [3 9 2]]

Vector:
[[3 8 9]]

Matrix + Vector:
[[10  9 14]
 [ 9 12  9]
 [ 6 17 11]]
```

---

### 5. Compute the sum of all elements, each column, and each row of a given array.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

array = np.random.randint(0, 11, size=(3, 3))

print("Array:\n", array)
print("\nSum of all elements:", np.sum(array))
print("\nSum of each column:", np.sum(array, axis=0))
print("\nSum of each row:", np.sum(array, axis=1))
```

```text
Output
Array:
[[2 7 3]
 [1 7 8]
 [4 8 10]]

Sum of all elements:
50

Sum of each column:
[ 7 22 21]

Sum of each row:
[12 16 22]
```

---

### 6. Extract numbers from an array greater than and less than a specified number.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

array = np.random.randint(0, 11, size=(3, 3))

print("Array:\n", array)
print("\nElements greater than 6:\n", array[array > 6])
print("\nElements less than 5:\n", array[array < 5])
```

```text
Output:
Array:
[[8 8 6]
 [4 1 3]
 [4 0 10]]

Elements greater than 6:
[ 8  8 10]

Elements less than 5:
[4 1 3 4 0]
```

---

### 7. Create a vector with values ranging from 15 to 55 and print all values except the first and last.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

vect = np.arange(15, 56)

print("Values except the first and last:", vect[1:-1])
```

```text
Output:
[16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39
 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54]
```

---

### 8. Insert a new axis into a 2D array.

```python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

array = np.random.randint(0, 10, size=(3, 4))

naxis0 = array[np.newaxis, :, :]
naxis1 = array[:, np.newaxis, :]
naxis2 = array[:, :, np.newaxis]

print("Original Array Shape:", array.shape)
print(array)
print("\nNew Axis along Axis 0 Shape:", naxis0.shape)
print(naxis0)
print("\nNew Axis along Axis 1 Shape:", naxis1.shape)
print(naxis1)
print("\nNew Axis along Axis 2 Shape:", naxis2.shape)
print(naxis2)
```

```text
Output:
Original Array Shape: (3, 4)
[[4 1 5 9]
 [5 8 0 1]
 [3 5 8 2]]

New Axis along Axis 0 Shape: (1, 3, 4)
[[[4 1 5 9]
  [5 8 0 1]
  [3 5 8 2]]]

New Axis along Axis 1 Shape: (3, 1, 4)
[[[4 1 5 9]]

 [[5 8 0 1]]

 [[3 5 8 2]]]

New Axis along Axis 2 Shape: (3, 4, 1)
[[[4]
  [1]
  [5]
  [9]]

 [[5]
  [8]
  [0]
  [1]]

 [[3]
  [5]
  [8]
  [2]]]
```
```
