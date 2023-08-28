## Introduction to Recursion

Recursion is a programming technique where a function calls itself to solve a problem. It allows breaking down complex problems into simpler subproblems, leading to elegant and concise code solutions. Recursion is based on the divide-and-conquer strategy.

## Important Techniques in Recursion

1. **Base Case:** Every recursive function must have a base case, which specifies the simplest scenario where the function can directly compute the result without further recursion.
    
2. **Recursive Case:** Define how to break the problem down into smaller subproblems. Each subproblem should be closer to the base case.
    
3. **Recursive Call:** In the function body, call the function itself with modified parameters to solve the smaller subproblem.


## Approach to Solving Recursion Problems

1. **Assumption:**
    - Begin by assuming that the recursive function works correctly for smaller instances of the problem.
    - This assumption is the "leap of faith" that you trust the function to solve simpler cases.
2. **Base Case Handling:**
    - Implement the base case(s) of the recursion explicitly, where the solution is known without further recursion.
    - These base cases act as starting points for the recursion and allow you to stop the recursive process.
3. **Recursive Structure:**
    - Express the problem in terms of the recursive function, breaking it down into smaller subproblems.
    - Use the assumption from step 1 to solve these subproblems recursively.
    - Combine the results of the subproblems to obtain the solution for the original problem.
 

## Important Patterns in Recursion 

1. [[Subsets]]
2. [[Subsequence 1]] 
3. Combinations
4. Permutations


# Things to keep in mind
### [[Handling Variables in Recursion]]

### [[Handling Answers in Recursion]]

### [[Recursion in Dynamic Programming]]

