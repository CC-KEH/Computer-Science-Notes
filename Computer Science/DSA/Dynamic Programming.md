Dynamic Programming (DP) is a powerful algorithmic technique used to solve optimization problems by breaking them down into smaller, overlapping subproblems. DP stores the solutions to these subproblems and reuses them to avoid redundant computations, resulting in significant efficiency improvements.

### Key Concepts:

1. **Overlapping Subproblems**:
   - DP problems can be decomposed into subproblems that are solved independently. However, these subproblems often overlap, meaning the same subproblem is solved multiple times. DP stores and reuses solutions to these subproblems.

2. **Optimal Substructure**:
   - DP problems exhibit optimal substructure, meaning that the optimal solution to the overall problem can be constructed from optimal solutions to its subproblems.

### Steps for Solving DP Problems:

1. **Define the Problem**:
   - Clearly define the problem you want to solve, including the objective and constraints.

2. **Identify Overlapping Subproblems**:
   - Recognize patterns of repeated subproblems within the problem. These are the building blocks for DP solutions.

3. **Formulate a Recursive Solution**:
   - Develop a recursive algorithm to solve the problem based on its subproblems. This may involve defining recurrence relations.

4. **Memoization or Tabulation**:
   - Implement DP using one of two common approaches:
     - **Memoization (Top-Down)**:
       - Use recursion to solve subproblems, but cache the results in a data structure (e.g., a dictionary or array) to avoid redundant computations.
     - **Tabulation (Bottom-Up)**:
       - Build a table or array to iteratively solve subproblems in a specific order, starting from the smallest subproblems and working towards the desired solution.

5. **Define the Base Cases**:
   - Specify the base cases that terminate the recursion. These are the simplest subproblems that can be solved directly.

6. **Optimize for Space (if necessary)**:
   - Sometimes, you can optimize space complexity by only storing the solutions to a limited number of subproblems rather than all of them.

### Example: Fibonacci Sequence

**Problem**: Calculate the nth Fibonacci number.

**DP Solution (Bottom-Up)**:

```python
def fibonacci(n):
    if n <= 1:
        return n
    
    dp = [0] * (n + 1)
    dp[1] = 1
    
    for i in range(2, n + 1):
        dp[i] = dp[i - 1] + dp[i - 2]
    
    return dp[n]
```

In this example, DP avoids redundant calculations by storing previously computed Fibonacci numbers in the `dp` array, starting from the base cases (0 and 1) and working up to the desired value of `n`.

### Benefits of Dynamic Programming:

- **Efficiency**: DP greatly improves the efficiency of algorithms by avoiding redundant computations, which can be especially important for complex problems.
- **Clarity**: DP solutions are often more intuitive and easier to understand than brute-force or recursive approaches.
- **Optimization**: DP can be used to optimize various problems, such as finding the shortest path, maximizing profits, or minimizing costs.



## Creating Recurrence Relation
1. Represent the problem in terms of index
2. Do all the possible stuff on that index according to the problem statement
3. Now do what is asked on that answer, min/max/sum/count or anything


## 3 Steps for converting Recursion to Dynamic Programming
1. Declare an array to store the answers from the below calls.
	```python
	dp = [] // size n+1
	```
2. Before returning the value from below call, store it in the array, then return it.
	```python
	dp.append(ans)
	return ans
	```
3. check just after the base condition if the answer for current call already exists in the array, if it does then simply return, else only then continue to the below code.
	```python
	if(base):
		do something
		return
	if(dp[n] is not None):
		return dp[n]
	
	else:
		computation code
	```
