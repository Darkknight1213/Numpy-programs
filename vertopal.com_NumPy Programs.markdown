---
jupyter:
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.12.7
  nbformat: 4
  nbformat_minor: 5
---

::: {#3aaefd83-8c4b-4a1a-8408-778acfd1e0a9 .cell .markdown}
### 1. Write a NumPy program to create a vector with values from 0 to 20 and change the sign of the numbers in the range from 9 to 15. {#1-write-a-numpy-program-to-create-a-vector-with-values-from-0-to-20-and-change-the-sign-of-the-numbers-in-the-range-from-9-to-15}
:::

::: {#d005bdc6-8528-4807-88ab-6d6901658668 .cell .code execution_count="11"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# ref no: 24900085

import numpy as np

# Inittializing an array with values from 0 to 20.
vector = np.arange(0, 21)
print(vector)

# changing the sign of numbers in the range from 9 to 15.
vector[9:16] *= -1
print(vector)
```

::: {.output .stream .stdout}
    [ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20]
    [  0   1   2   3   4   5   6   7   8  -9 -10 -11 -12 -13 -14 -15  16  17
      18  19  20]
:::
:::

::: {#64585fd2-a810-4b93-a361-bfe42f0f4c77 .cell .markdown}
### 2. Write a NumPy program to create a 10x10 matrix, in which the elements on the borders will be equal to 1, and inside 0. {#2-write-a-numpy-program-to-create-a-10x10-matrix-in-which-the-elements-on-the-borders-will-be-equal-to-1-and-inside-0}
:::

::: {#0e60e82a-8093-4868-8918-160316c5d6fe .cell .code execution_count="17"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# ref no: 24900085

import numpy as np

mat = np.zeros((10,10), dtype=int)

mat[0] = mat[-1] = mat[:, 0] = mat = 1

print(mat)
```

::: {.output .stream .stdout}
    [[1 1 1 1 1 1 1 1 1 1]
     [1 0 0 0 0 0 0 0 0 0]
     [1 0 0 0 0 0 0 0 0 0]
     [1 0 0 0 0 0 0 0 0 0]
     [1 0 0 0 0 0 0 0 0 0]
     [1 0 0 0 0 0 0 0 0 0]
     [1 0 0 0 0 0 0 0 0 0]
     [1 0 0 0 0 0 0 0 0 0]
     [1 0 0 0 0 0 0 0 0 0]
     [1 1 1 1 1 1 1 1 1 1]]
:::
:::

::: {#2fef8ecc-e3fe-49c0-b699-b8acd3c03160 .cell .markdown}
### 3. Write a NumPy program to create an array of 10 zeros,10 ones, 10 fives {#3-write-a-numpy-program-to-create-an-array-of-10-zeros10-ones-10-fives}
:::

::: {#fa68342f-efed-404e-be62-f940755b6306 .cell .code execution_count="25"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# ref no: 24900085

import numpy as np

zeros = np.zeros(10)
print(zeros)

ones = np.ones(10)
print(ones)

fives = np.full(10, 5)
print(fives)
```

::: {.output .stream .stdout}
    [0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
    [1. 1. 1. 1. 1. 1. 1. 1. 1. 1.]
    [5 5 5 5 5 5 5 5 5 5]
:::
:::

::: {#a74e35b7-22fa-455e-87a4-418eb5361495 .cell .markdown}
### 4. Write a NumPy program to add a vector to each row of a given matrix. {#4-write-a-numpy-program-to-add-a-vector-to-each-row-of-a-given-matrix}
:::

::: {#bc0b7891-6643-42ce-bd41-c2eac1537446 .cell .code execution_count="40"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# ref no: 24900085

import numpy as np

mat = np.random.randint(0, 10, size=(3,3))
print("Matrix:")
print(mat)

vect = np.random.randint(0, 10, size=(1,3))
print("\nVector:")
print(vect)

added_matrix = mat + vect
print("\nMatrix + Vector:")
print(added_matrix)
```

::: {.output .stream .stdout}
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
:::
:::

::: {#a6a949e4-7c69-4e1c-9c95-f9b059b009a0 .cell .markdown}
### 5. Write a NumPy program to compute sum of all elements, sum of each column and sum of each row of a given array. {#5-write-a-numpy-program-to-compute-sum-of-all-elements-sum-of-each-column-and-sum-of-each-row-of-a-given-array}
:::

::: {#44c09b8f-e603-47d2-a23b-d0ce31b86dd1 .cell .code execution_count="49"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# ref no: 24900085

import numpy as np

array = np.random.randint(0, 11, size=(3,3))
print("Array:\n", array, sep="")

print("\nSum of all elements:\n",np.sum(array))

print("\nSum of each column:\n", np.sum(array, axis=0))

print("\nSum of each row:\n", np.sum(array, axis=1))
```

::: {.output .stream .stdout}
    Array:
    [[ 2  7  3]
     [ 1  7  8]
     [ 4  8 10]]

    Sum of all elements:
     50

    Sum of each column:
     [ 7 22 21]

    Sum of each row:
     [12 16 22]
:::
:::

::: {#fa3aea72-87cb-451b-8a8c-2c01cc4d7888 .cell .markdown}
### 6. Write a NumPy program to extract all numbers from a given array which are less and greater than a specified number. {#6-write-a-numpy-program-to-extract-all-numbers-from-a-given-array-which-are-less-and-greater-than-a-specified-number}
:::

::: {#5a2d6ecf-647a-43fe-b49d-ce83bbcdd393 .cell .code execution_count="57"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

array = np.random.randint(0, 11, size=(3,3))

print("The given array is: \n", array, sep="")

print("\nElements greater Than 6 in the array:\n", array[array>6])

print("\nNumbers lesser than 5 in the array:\n", array[array<5])
```

::: {.output .stream .stdout}
    The given array is: 
    [[ 8  8  6]
     [ 4  1  3]
     [ 4  0 10]]

    Elements greater Than 6 in the array:
     [ 8  8 10]

    Numbers lesser than 5 in the array:
     [4 1 3 4 0]
:::
:::

::: {#481414f0-8d49-44ac-9ea6-aa4ce610e623 .cell .markdown}
### 7. Write a NumPy program to create a vector with values ​​ranging from 15 to 55 and print all values ​​except the first and last. {#7-write-a-numpy-program-to-create-a-vector-with-values-ranging-from-15-to-55-and-print-all-values-except-the-first-and-last}
:::

::: {#b35fcba0-1030-4ef6-969d-52ee6453b682 .cell .code execution_count="63"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085

import numpy as np

vect = np.arange(15, 56)

print("Values except the first and last:", vect[1:-1])
```

::: {.output .stream .stdout}
    Values except the first and last: [16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39
     40 41 42 43 44 45 46 47 48 49 50 51 52 53 54]
:::
:::

::: {#3e8d88cf-891b-490e-a8f7-b9e5df3d549f .cell .markdown}
### 8. Write a NumPy program to insert a new axis within a 2-D array.2-D array of shape (3, 4) {#8-write-a-numpy-program-to-insert-a-new-axis-within-a-2-d-array2-d-array-of-shape-3-4}
:::

::: {#01d50c7a-1d1b-4fc7-a9c4-f540bba53a63 .cell .code execution_count="71"}
``` python
# Developed by: Mohamed Riyaz Ahamed
# Reference Number: 24900085
import numpy as np

# Create a 2-D array of shape (3, 4)
array = np.random.randint(0, 10, size=(3,4))

naxis0 = array[np.newaxis, :, :]

naxis1 = array[:, np.newaxis, :]

naxix2 = array[:, :, np.newaxis]

print("Original Array Shape:", array.shape)
print(array)
print("\nNew Axis along Axis 0 Shape:", naxis0.shape)
print(naxis0)
print("\nNew Axis along Axis 1 Shape:", naxis1.shape)
print(naxis1)
print("\nNew Axis along Axis 2 Shape:", naxix2.shape)
print(naxix2)

```

::: {.output .stream .stdout}
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
:::
:::

::: {#d80d34ed-28a1-40d4-b68b-065d7bc24a5f .cell .code}
``` python
```
:::
