# Your Task

Write a method that calculates the sum of all integers in an array. Your solution will have **O(n) complexity** because you must examine each element exactly once.

**Important**: Implement the summation using a loop to understand the O(n) behavior. Built-in LINQ methods like `.Sum()` or `.Aggregate()` are not allowed for this exercise.

# Method Signature

```cs
public static int SumArray(int[] numbers)
{
    // Your code here
}
```

# Expected Results

```cs
SumArray([1, 2, 3, 4, 5]) -> 15
SumArray([10, 20, 30]) -> 60
SumArray([-5, 5, -10, 10]) -> 0
```

# Hints

💡 1. Initialize a variable to store the running total, starting at 0

💡 2. Use a for loop or foreach to iterate through each element in the array

💡 3. Add each element to your running total as you visit it - this single pass through the array is what makes it O(n)
