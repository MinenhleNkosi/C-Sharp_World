```cs
using System;

public class Solution
{
    public static bool HasDuplicatesNaive(int[] numbers)
    {
        // Use nested loops to compare every pair of elements
        // Return true if any duplicate is found
        bool hasDuplicate = false;

        for (int i = 0; i < numbers.Length; i++)
        {
            for (int j = i + 1; j < numbers.Length; j++)
            {
                if (numbers[i] == numbers[j])
                {
                    hasDuplicate = true;
                }
            }
        }
        return hasDuplicate;
    }
}
```
