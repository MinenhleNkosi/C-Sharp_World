```cs
using System;

public class Solution
{
    public static int SumAll(params int[] numbers)
    {
        // Your code here
        int sum = 0;

        if (numbers.Length == 0)
        {
            return 0;
        }

        foreach (int number in numbers)
        {
            sum += number;
        }

        return sum;
    }
}
```
