# Module Title: Python Fundamentals and Optimization Techniques

## Example 2: Implementing a Function to Calculate Factorial

### 1. Introduction
In this section, we will explore the significance of calculating the factorial of a number, particularly in the fields of Robotics, semiconductors, and consumer electronics. The factorial function is a fundamental concept in mathematics and programming, often used in algorithms related to combinatorics, probability, and statistical analysis. In robotics, for instance, factorial calculations can help in optimizing paths for robotic movement by evaluating permutations and combinations of possible routes. Similarly, in consumer electronics, it can be used in signal processing algorithms that require statistical computations.

### 2. Code Snippet
Here’s a Python function that calculates the factorial of a number using recursion. This implementation includes error handling and follows best practices for clarity and efficiency.

```python
def factorial(n):
    """
    Calculate the factorial of a non-negative integer n.
    
    Parameters:
    n (int): A non-negative integer whose factorial is to be computed.
    
    Returns:
    int: The factorial of n.
    
    Raises:
    ValueError: If n is negative.
    """
    # Check if the input is a negative number
    if n < 0:
        raise ValueError("Input must be a non-negative integer.")
    
    # Base case for recursion
    if n == 0 or n == 1:
        return 1
    
    # Recursive case
    return n * factorial(n - 1)

# Example usage
try:
    result = factorial(5)
    print(f"The factorial of 5 is: {result}")  # Output: The factorial of 5 is: 120
except ValueError as e:
    print(e)
```

### 3. Explanation
- **Function Definition**: The `factorial` function is defined to take one parameter `n`, which is expected to be a non-negative integer.
- **Error Handling**: The first conditional checks if `n` is negative. If so, it raises a `ValueError`, ensuring that the function only processes valid inputs.
- **Base Case**: The function checks if `n` is either `0` or `1`. In both cases, the factorial is defined to be `1`, which serves as the base case for our recursion.
- **Recursive Case**: For values greater than `1`, the function calls itself with `n - 1`, multiplying the current value of `n` by the factorial of `n - 1`. This recursive approach effectively breaks down the problem into smaller subproblems until it reaches the base case.
- **Example Usage**: The code includes a try-except block to demonstrate how to call the function and handle potential errors gracefully.

### 4. Application
In the context of Robotics, semiconductors, and consumer electronics, calculating factorials can be essential for optimizing algorithms that require combinatorial calculations. For example:
- **Path Optimization in Robotics**: When programming a robot to navigate through a grid or maze, determining the number of possible paths can help in selecting the most efficient route. Factorials are used to calculate permutations of movements.
- **Signal Processing**: In consumer electronics, signal processing algorithms often involve statistical analyses where factorials are necessary for calculating probabilities and combinations, such as in noise reduction or data compression techniques.

By mastering such fundamental concepts as factorial calculations, you will build a strong foundation for tackling more complex problems in your projects involving data processing and automation. This knowledge not only enhances your coding skills but also prepares you for real-world applications in your field of interest.

### Integration
The content provided is structured with clear headings and sections to facilitate easy navigation and integration into your learning platform. Each section builds upon the key concepts discussed in your previous lectures on data types and structures, reinforcing your understanding through practical application and hands-on coding experience.