# ECE-2112-PA-2

**Made by: Julius Miguel S. Mendizabal | 2ECE-C**

The content of this repository contains the Programming Assignment 2 for our course "Advance Computer Programming" this S.Y. 2025-2026. This project covers two python problems pertaining to Module 2 - Numerical Python (Numpy).

# **1. Normalization Problem**

In this problem, create a random 5×5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy

The following functions and methods were used in this problem:

• `np.random.random((n,m))` - this function generates random floats in the 0-1 range then stores it to an array with the shape of n number of rows and m number of columns.

The code below creates a 2-dimensional 5×5 array with random values, and stores it to the variable 'X'.
```python
X = np.random.random((5,5))
```

Here, we use the normalization formula for variable 'X'. This subtracts the value in the array from their mean and divides it with its standard deviation, using the functions `X.mean()` and `X.std()`.
```python
X_normalized = (X - X.mean()) / X.std()
```

We were also tasked to save the normalized ndarray as "X_normalized.npy". 
•np.save("<array_file_name>.npy", <array_name>) - this command saves the NumPy array permanently as a binary .npy file.

```python
np.save("X_normalized.npy", X_normalized)
```

# **2. Divisible by 3 Problem**

In this problem, create a 10 x 10 ndarray, which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

The following functions and methods were used in this problem:

• `np.arange(1, 101)` - this function generates integers starting from 1 up to 100 ([101] is excluded), storing it to a 1-dimensional array.
• `.reshape(10, 10)` - this code reshapes the 1D array of 100 elements into a 10×10 2D array.
• `** 2` - this operation then squares the array element-wise.

Combining all the functions above, we can assign the 10x10 array containing the squares of the first 100 positive integers to variable 'A'.
```python
A = np.arange(1, 101).reshape(10, 10) ** 2
```

To find the integers that are divisible by 3, we use the modulus (%) operation as an argument index in accessing the elements in the array. 
```python
div_by_3 = A[A % 3 == 0]
```
We were also tasked to save the result as div_by_3.npy
```python
np.save("div_by_3.npy", div_by_3)
```

Thank you for reading! 

To see the main python program for Programming Assignment 2, click this link and download. Open on Jupyter Notebook, then run all cells.


