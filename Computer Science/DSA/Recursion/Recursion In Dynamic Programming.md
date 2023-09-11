Recursion and dynamic programming (DP) are closely related. In some cases, recursive solutions can be inefficient due to repeated calculations. DP optimizes this by storing intermediate results in a table.

1. **Top-Down DP:** Convert the recursive solution into a DP solution by memoization. Store the results of recursive calls in a table to avoid redundant computations.
    
2. **Bottom-Up DP:** Build the solution iteratively, solving subproblems in a specific order and using previously computed results.


## Example: Fibonacci Sequence

```python
# Recursive Fibonacci
def fib_recursive(n):
    if n <= 1:
        return n
    return fib_recursive(n - 1) + fib_recursive(n - 2)

# Top-Down DP Fibonacci
def fib_top_down(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fib_top_down(n - 1, memo) + fib_top_down(n - 2, memo)
    return memo[n]
```

## Factorial Calculation

```python
def calculate_factorial(n, memo):
    # Base Case: Factorial of 0 is 1
    if n == 0:
        return 1
    
    # Check if the factorial of n is already computed and stored in memo
    if memo[n] != -1:
        return memo[n]
    
    # Recursive Call: Calculate factorial of (n - 1)
    factorial_of_n_minus_1 = calculate_factorial(n - 1, memo)
    
    # Calculate factorial of n by multiplying with n
    memo[n] = n * factorial_of_n_minus_1
    
    return memo[n]

def factorial(n):
    # Initialize an array to store intermediate results (-1 indicates not computed)
    memo = [-1] * (n + 1)
    
    # Call the recursive function
    result = calculate_factorial(n, memo)
    
    return result

# Example input
number = 5

# Calculate and print the factorial
print(f"The factorial of {number} is {factorial(number)}"
```
