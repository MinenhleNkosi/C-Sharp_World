# Your Task

Create two overloaded `Add` methods:

1. `Add(int a, int b)` - returns the sum of two integers
2. `Add(int a, int b, int c)` - returns the sum of three integers

## Method Signatures

```cs
public static int Add(int a, int b)
public static int Add(int a, int b, int c)
```

## Expected Results

```cs
Add(5, 3) -> 8
Add(1, 2, 3) -> 6
Add(-5, 5) -> 0
Add(10, 20, 30) -> 60
```

## Hints

- Both methods should have the exact same name: `Add`
- The first method takes 2 parameters, the second takes 3 parameters
- Use the `return` keyword to send back the sum of all parameters

## Example Code

```cs
using System;

public class Solution
{
    // Create an Add method that takes 2 integers and returns their sum
    public static int Add(int a, int b)
    {
        // Your code here
    }

    // Create an overloaded Add method that takes 3 integers and returns their sum
    public static int Add(int a, int b, int c)
    {
        // Your code here
    }
}
```
