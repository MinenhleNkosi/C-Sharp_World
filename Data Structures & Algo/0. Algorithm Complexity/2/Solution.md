```cs
using System;
using System.Collections.Generic;

public class Solution
{
    public static bool HasDuplicatesOptimized(int[] numbers)
    {
        // Your code here
        var hasDuplicate = new HashSet<int>();
        bool duplicateCheck = false;

        foreach (var number in numbers)
        {
            if (!hasDuplicate.Add(number))
            {
                duplicateCheck = true;
            }
        }
        return duplicateCheck;
    }
}
```
