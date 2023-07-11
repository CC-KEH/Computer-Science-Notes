**Binary search is a fundamental algorithm used to efficiently search for an element in a sorted array or list. It follows a divide-and-conquer approach and repeatedly divides the search space in half until the target element is found or the search space is exhausted.** 

**Time Complexity: O(log n)**

## Algorithm

**The binary search algorithm works as follows:

```python
def binary_search(arr, x):
    low = 0
    high = len(arr) - 1
    mid = 0
    while low <= high:
        mid = (high + low) // 2
        # If x is greater, ignore left half`
        if arr[mid] < x:
            low = mid + 1
        # If x is smaller, ignore right half`
        elif arr[mid] > x:
            high = mid - 1
        # means x is present at mid
        else:
            return mid
    # If we reach here, then the element was not present`
    return -1
```

## Use Cases

1. **Searching in Sorted Arrays**: Binary search is commonly used to find a specific element or determine if an element exists in a sorted array. It provides an efficient way to search through large datasets in logarithmic time complexity.

2. **Finding Bounds and Ranges**: Binary search can be used to find the lower and upper bounds of a target element in a sorted array. It helps in determining the range or count of elements that satisfy certain conditions.

3. **Bitonic Arrays**: A bitonic array is an array that is first sorted in ascending order and then sorted in descending order. Binary search can be used to find the maximum element or pivot element in a bitonic array efficiently.

4. **Rotated Arrays**: Binary search can be applied to find a target element in a rotated sorted array. By comparing the middle element with the endpoints, the search space can be narrowed down efficiently.

5. **Square Root Approximation**: Binary search can be used to approximate the square root of a given number with a specified precision. It provides a fast convergence to the approximate value.


## Patterns to Identify Binary Search Problems

1. **Sorted Data**: Look for problems involving sorted data structures such as arrays or lists. Binary search typically works on sorted data to take advantage of the divide-and-conquer strategy.
  
2. **Search Space Reduction**: If the problem involves reducing the search space in each iteration by discarding one half, it could be a potential binary search problem.
 
3. **Decision or Optimization**: Binary search is often used when you need to make a decision or optimize a certain parameter. It helps in finding the exact solution or narrowing down the range efficiently.

4. **Monotonicity**: Problems that exhibit monotonic behavior, such as monotonic increasing or decreasing sequences, are good candidates for binary search.

5. **Hidden Sequence**: Check if there is a hidden sequence that you will be following to get the target value, e.g. square root of a number, in this case you are not given array but to get to the square root you will be following a sequence. 



## Important Questions

#dsaquestions 

1. [Count occurrences in Sorted array](https://takeuforward.org/data-structure/count-occurrences-in-sorted-array/)
2. [Search in Rotated Sorted array I](https://leetcode.com/problems/search-in-rotated-sorted-array/description/)
3. [Search in Rotated Sorted array II](https://leetcode.com/problems/search-in-rotated-sorted-array-ii/)
4. [Single element in a Sorted array](https://leetcode.com/problems/single-element-in-a-sorted-array/)
