# ECE2112_PA2_LAO_JAREDRUSELL
This repository contains the contents of my programming assignment 2 for ECE 2112, focused on the fundamentals used in Numpy

ECE2112 - JARED RUSELL CHUA LAO, 2ECE-B
September 3, 2026

A. REPRODUCIBLE NORMALIZATION PROBLEM

Goal: The goal of this portion of the assignment is to create a 5x5 array, using the same array to get the mean and standard deviation, and display the required components. 

1. np.random.seed(2112) - Takes from the specified random seed and creates an array

2. X = np.random.randint(10, 101, size=(5, 5)) = gets a random integer from the array and names it "X", aka the random number generator
  
3. X_normalized = ((X-np.mean(X))/np.std(X)) = Gets the Z-score using the formula (X-mean)/sd, creating a an array that follows the formula

3a. X = The random number from the previous code

3b. np.mean(X) = a function that uses the built-in Numpy libraries to get the mean of X

3c. np.std(X) = a function that gets the standard deviation via a built-in function in Numpy

5. standard_deviation = np.std(X_normalized) = gets the standard deviation based on the X_normalized array and renames it.

6. mean = np.mean(X_normalized) = gets the mean from the X_normalized array

7. np.save("X_normalized.npy",X_normalized) = saves the array, X_normalized named as "X_normalized.npy" in Jupyter Home


B. CUBES DIVISIBLE BY 4 PROBLEM

Goal: Create a 10x10 array using the first 100 positive integers, all raised to three, while using a boolean condition to get all of the elements that are divisible by 4 

1. C = (np.arange(1,101)**3).reshape(10, 10) = creates a 10x10 array named C with 1-100 in the array all raised to three

1a.  np.arange(1,101) = creates an array that starts with 1 and ends with 100, excluding 101

1b. reshape(10,10) = the portion that creates an array that is 10x10 instead of the default array structure

2. C.shape = acquires the shape of the array, C, which was reshaped to be a 10x10 array

3. div_by_4 = C[C%4==0] = Uses a boolean condition that acquires all the elements in the array C, that is divisible by 4 and yields 0, meaning that it is perfectly divisible without any decimals.

4. div_by_4.size = A function that counts all of the elements inside the array, div_by_4

5. np.save("div_by_4.npy", div_by_4) = Saves the array div_by_4 in Jupyter home as a .npy file


C. ABOVE-MEAN SQUARES PROBLEM

Goal: Create a 6x6 array named S has the first 36 positive integers, and using those elements to acquire the array's mean and elements greater than the mean. 

1. S = (np.arange(1,37)**2).reshape(6,6) = creates a 6x6 array with the integers 1-36, excluding 37, despite being in the array range, while the entire array is reshaped to 6x6.

2. S_mean = np.mean(S) = acquires the mean of the array, and naming it S_mean

3. above_mean = S[S>S_mean] = Acquires all of the elements that follow the indicated condition, which is to be greater than the mean.

4. above_mean.size = using the function .size, it acquires the number of elements that are above the mean

5. np.save("above_mean.npy", above_mean) = Saves the array "above_mean" as an .npy file in Jupyter Home. 


