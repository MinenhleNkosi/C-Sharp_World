```cs
using System;

public class Solution
{
    public static int SumArray(int[] numbers)
    {
        // Your code here
        int sum = 0;

        for (int i = 0; i < numbers.Length; i++)
        {
            sum += numbers[i];
        }
        return sum;
    }
}
```
