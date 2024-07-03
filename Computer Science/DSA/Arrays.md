## Introduction
An array is a data structure that stores a fixed-size sequential collection of elements of the same type. 
- In java array stores elements in non continuous manner it depends on JVM.
- In C++ and Python it stores in continuous manners


## Important Functions
#### Python 
```python
len(arr)  # O(1)
arr.insert(index, element)  # O(n)
arr.remove(element)  # O(n)
arr.pop(index)  # O(n) (if index is not the last element)
arr.pop()       # O(1)
arr.index(element)  # O(n)
arr.count(element)      # O(n) Returns the number of occurrences of the element
arr.sort()              # O(n log n) Sorts the array in ascending order
arr.sort(reverse=True)  # O(n log n) Sorts the array in descending order
arr.reverse()           # O(n) Reverses the array
```
#### C++
```cpp
std::vector<int> vec; // example vector declaration
vec.size();                // O(1)
vec.insert(vec.begin() + index, element);  // O(n)
vec.erase(std::remove(vec.begin(), vec.end(), element), vec.end());  // O(n)
vec.erase(vec.begin() + index);  // O(n) (if index is not the last element)
vec.pop_back();          // O(1)
std::find(vec.begin(), vec.end(), element);  // O(n)
std::count(vec.begin(), vec.end(), element);  // O(n) freq of element 
std::sort(vec.begin(), vec.end());            // O(n log n) ascend
std::sort(vec.begin(), vec.end(), std::greater<int>());  // O(n log n) descend
std::reverse(vec.begin(), vec.end());         // O(n) Reverse
```

## How Array works?

```java
%% In C++ %%
int[] arr;       //Declaration, at compile time
arr = {1,2,3};   //Initialisation, Object is created here in Heap memory, at runtime
                // runtime memory allocation is also known as dynamic memory allocation
```

```python
%% In Python %%
arr = [1, 2, 3]  # Declaration and initialization, both done at runtime
```


## Dynamic Vs Static
- Dynamic Arrays comes with the overhead of space allocation. Example, if the array is completely filled but we want to add more elements, then in that case the compiler will make an array of size len(arr) + 2 times len(arr), in a different location. So if the size of array was 10 then it will create a new array of size 30.
- Static Arrays will cause Index out of bound error.



## Important patterns in core array problems
1. **Two Pointer Technique**
    - Used for problems like finding pairs in a sorted array that sum to a specific value.
2. **Sliding Window Technique**
    - Useful for problems like finding the maximum sum subarray of a fixed size.
3. **Prefix Sum and Suffix Sum Arrays**
    - Helps in solving range sum queries efficiently.
4. **Binary Search on Arrays**
    - Useful for finding elements or checking conditions in sorted arrays.
5. **Merge Intervals**
    - Used in problems like merging overlapping intervals.
6. **Dutch National Flag Algorithm**
    - Efficiently solves problems related to sorting arrays with three distinct values.



#dsaquestions 
1. [Count Reverse Pairs](https://takeuforward.org/data-structure/count-reverse-pairs/)
2. [Count inversions in an array](https://takeuforward.org/data-structure/count-inversions-in-an-array/)
3. [Find the repeating and missing numbers](https://takeuforward.org/data-structure/find-the-repeating-and-missing-numbers/) ^a9bdbd
4. [Merge Overlapping Sub-intervals](https://takeuforward.org/data-structure/merge-overlapping-sub-intervals/)
5. [Count Inversions](https://takeuforward.org/data-structure/count-inversions-in-an-array/)
6. [Count Reverse Pairs](https://takeuforward.org/data-structure/count-reverse-pairs/)

