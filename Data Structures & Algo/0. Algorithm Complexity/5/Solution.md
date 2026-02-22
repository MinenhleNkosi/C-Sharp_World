```cs
using System;

public class Solution
{
    public static int[] CompareOperationCounts(int n)
    {
        // Your code here
        int linearCount = 0;
        int quadraticCount = 0;

        for (int i = 0; i < n; i++)
        {
            linearCount++;
        }

        for (int i = 0; i < n; i++)
        {
            for (int j = 0; j < n; j++)
            {
                quadraticCount++;
            }
        }

        return [linearCount, quadraticCount];
    }
}
```
