```cs
using System;

public class Solution
{
    public static int CountBinarySearchSteps(int[] sortedArray, int target)
    {
        // Implement binary search and count each comparison
        // Return the total number of steps (comparisons) made
        int left = 0;
        int right = sortedArray.Length - 1;
        int steps = 0;

        while (left <= right)
        {
            int middleValue = left + (right - left) / 2;
            steps++;

            if (sortedArray[middleValue] == target)
            {
                return steps;
            }
            else if (sortedArray[middleValue] < target)
            {
                left = middleValue + 1;
            }
            else {
                right = middleValue - 1;
            }
        }
        return steps;
    }
}
```
