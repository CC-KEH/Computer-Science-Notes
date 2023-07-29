**An array is a data structure that stores a fixed-size sequential collection of elements of the same type. In java array stores elements in non continuous manner it depends on JVM, whereas in C++ it stores in continuous manner**


## Important Functions

#### 1. `System.arraycopy()`
The `System.arraycopy()` method is used to copy elements from one array to another. It provides a fast and efficient way to copy arrays. Here's an example of how to use it:
``` java
int[] sourceArray = {1, 2, 3, 4, 5}; 
int[] destinationArray = new int[5]; System.arraycopy(sourceArray,SrcArrStart=0,destinationArray,destArrStart=0, sourceArray.length);
```


#### 2. `Arrays.copyOf()`

The `Arrays.copyOf()` method is used to create a new array with a specified length and copy elements from the original array into it. Here's an example:
```java
int[] numbers = {1, 2, 3, 4, 5};
int[] copiedArray = Arrays.copyOf(numbers, numbers.length); // creates a copy of the numbers array

Case 1:
int[] numbers = {1, 2, 3, 4, 5};
int[] copiedArray = Arrays.copyOf(numbers, 8); // {1, 2, 3, 4, 5, 0, 0, 0}
len(numbers) < 8 => so it fills the later array with default value.
the default value is `0` for int. 

Case 2:
int[] numbers = {1, 2, 3, 4, 5};
int[] copiedArray = Arrays.copyOf(numbers, 3); //{1,2,3}
Discards after 3, since len(numbers) > 3
```


#### 3. `Arrays.fill()`

The `Arrays.fill()` method is used to fill the elements of an array with a specified value. It replaces all existing elements with the given value. Here's an example:

```java
int[] numbers = new int[5];
Arrays.fill(numbers, 0); // fills the array with zeros
```


## How Array works?

```java
int[] arr;       //Declaration, at compile time
arr = {1,2,3};   //Initialisation, Object is created here in Heap memory, at runtime
                runtime memory allocation is also known as dynamic memory allocation
```



## Important patterns in core array problems








#dsaquestions 
1. [Count Reverse Pairs](https://takeuforward.org/data-structure/count-reverse-pairs/)
2. [Count inversions in an array](https://takeuforward.org/data-structure/count-inversions-in-an-array/)
3. [Find the repeating and missing numbers](https://takeuforward.org/data-structure/find-the-repeating-and-missing-numbers/) ^a9bdbd
4. [Merge Overlapping Sub-intervals](https://takeuforward.org/data-structure/merge-overlapping-sub-intervals/)
5. [Count Inversions](https://takeuforward.org/data-structure/count-inversions-in-an-array/)
6. [Count Reverse Pairs](https://takeuforward.org/data-structure/count-reverse-pairs/)

