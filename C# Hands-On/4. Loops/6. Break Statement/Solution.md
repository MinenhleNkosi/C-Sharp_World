```cs
using System;

public class Solution
{
    public static void FindFirstDivisibleBySeven()
    {
        // Use a for loop to iterate from 1 to 100
        // Find the first number divisible by 7
        // Print it and use break to exit the loop immediately
        // Your code here
        for (int i = 1; i <= 100; i++)
        {
            if (i % 7 == 0)
            {
                Console.WriteLine(i);
                break;
            }
        }
    }
}
```
