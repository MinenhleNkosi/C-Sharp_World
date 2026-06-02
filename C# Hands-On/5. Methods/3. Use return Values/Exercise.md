# Your Task

Create two methods:

1. **Add** - Takes two integers and returns their sum
2. **Calculate** - Takes three integers (a, b, c) and returns `Add(a, b) * c`

The key is to call the `Add` method from within `Calculate` and use its return value.

## Method Signatures

```cs
public static int Add(int x, int y)
public static int Calculate(int a, int b, int c)
```

## Expected Results

```cs
Calculate(2, 3, 4) -> 20   // (2 + 3) * 4 = 20
Calculate(5, 5, 2) -> 20   // (5 + 5) * 2 = 20
Calculate(0, 10, 5) -> 50  // (0 + 10) * 5 = 50
```

## Hints

- First implement the `Add` method to return `x + y`
- In `Calculate`, call `Add(a, b)` and store the result in a variable
- Multiply the stored sum by `c` and return that result

## Example Code

```cs
using System;

public class Solution
{
    // Step 1: Create an Add method that takes two integers and returns their sum
    public static int Add(int x, int y)
    {
        // Your code here
    }

    // Step 2: Use the Add method's return value in a calculation
    // Calculate: Add(a, b) multiplied by c
    public static int Calculate(int a, int b, int c)
    {
        // Your code here - call Add and use its result
    }
}
```
