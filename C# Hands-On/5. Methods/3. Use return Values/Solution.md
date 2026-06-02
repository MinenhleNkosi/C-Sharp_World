```cs
using System;

public class Solution
{
    // Step 1: Create an Add method that takes two integers and returns their sum
    public static int Add(int x, int y)
    {
        // Your code here
        return x + y;
    }

    // Step 2: Use the Add method's return value in a calculation
    // Calculate: Add(a, b) multiplied by c
    public static int Calculate(int a, int b, int c)
    {
        // Your code here - call Add and use its result
        return Add(a, b) * c;
    }
}
```
