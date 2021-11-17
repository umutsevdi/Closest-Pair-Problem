# Closest-Pair-Problem
In this problem, a set of n points are given on the 2D plane. In this problem, we have to find the pair of points, whose distance is minimum.

To solve this problem, we have to divide points into two halves, after that smallest distance between two points is calculated in a recursive way. Using distances from the middle line, the points are separated into some strips. We will find the smallest distance from the strip array. At first two lists are created with data points, one list will hold points which are sorted on x values, another will hold data points, sorted on y values.

The time complexity of this algorithm will be O(n log n).
```
Input:
A set of different points are given. (2, 3), (12, 30), (40, 50), (5, 1), (12, 10), (3, 4)
Output:
Find the minimum distance from each pair of given points.
Here the minimum distance is: 1.41421 unit.
```
# About the Implementation
* In the implementation of the algorithm `quick-sort` is used on sorting the points based on x axis.
* There are no global variables, all are assigned in function scopes or allocated with `malloc()` function.
* All forms of array accessing is done with pointers.
* Algorithm displays each function when they are called.
* It runs recursively for better performance.

# Functions
## getDistance(point* from, point* to)
* getDistance function finds the distance between two points and returns double.

## swap( point* a, point* b)
* Swaps the values of given points.
## quickSort(point* array, int low, int high)
* Quick sort is used to sort points based on x axis. It uses Divide and Conquer algorithm to iterate over values recursively. 
## partition(point* array, int low, int high)
* This function is called at each iteration to find the pivot.
## bruteForce(point* array, int low, int high, double* result)
* Calculates the distance between each point combination within given and returns the lowest distance.
## recursive(point* array, int low, int high, double* d)
* This function iterates through the array recursively until it reaches to smallest possible division. Then calls `bruteForce` function for those values.
## printArray(point* array, int low, int high)
* Prints all elements of the array.

# Complexity Analysis
* Quick Sort algorithm uses `n*log(n)`.
* `T(n) = 2T(N/2) + O(N) + O(N) = 2T(N/2) + 3O(N) = N*log(N)`