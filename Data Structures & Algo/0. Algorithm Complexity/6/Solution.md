```cs
using System;
using System.Collections.Generic;

public class Solution
{
    public static int[] ComplexityCapstone(int[] numbers)
    {
        // For empty array
        if (numbers.Length == 0)
        {
            return [0, 0, 0];
        }

        // For HashSet
        int hasDuplicateHashSet = 0;
        HashSet<int> hasDuplicate = new HashSet<int>();

        for (int i = 0; i < numbers.Length; i++)
        {
            if (!hasDuplicate.Add(numbers[i]))
            {
                hasDuplicateHashSet = 1;
                break;
            }
        }

        // For nested loops
        int hasDuplicateNaive = 0;

        for (int i = 0; i < numbers.Length; i++)
        {
            for (int j = i + 1; j < numbers.Length; j++)
            {
                if (numbers[i] == numbers[j])
                {
                    hasDuplicateNaive = 1;
                    break;
                }
            }

            if (hasDuplicateNaive == 1)
            {
                break;
            }
        }

        // Sorting the array manually
        int temp;

        int[] sorted = new int[numbers.Length];
        for (int i = 0; i < numbers.Length; i++)
        {
            sorted[i] = numbers[i];
        }

        for (int i = 0; i < sorted.Length - 1; i++)
        {
            for (int j = 0; j < sorted.Length - i - 1; j++)
            {
                if (sorted[j] > sorted[j + 1])
                {
                    temp = sorted[j];
                    sorted[j] = sorted[j + 1];
                    sorted[j + 1] = temp;
                }
            }
        }


        // For Binary Search
        int binarySearchStepsForMiddle = 0;
        int target = sorted[sorted.Length / 2];

        int firstValue = 0;
        int lastValue = sorted.Length - 1;

        while (firstValue <= lastValue)
        {
            int middleValue = firstValue  + (lastValue - firstValue) / 2;
            binarySearchStepsForMiddle++;

            if (sorted[middleValue] == target)
            {
                break;
            }
            else if (sorted[middleValue] < target)
            {
                firstValue = middleValue + 1;
            }
            else
            {
                lastValue = middleValue - 1;
            }
        }

        return [hasDuplicateNaive, hasDuplicateHashSet, binarySearchStepsForMiddle];

    }
}
```
