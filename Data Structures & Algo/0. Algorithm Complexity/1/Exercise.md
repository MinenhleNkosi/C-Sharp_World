# Your Task

Write a method that checks if an array contains duplicate values using **nested for loops only**. Do not use HashSet, LINQ, or sorting - the goal is to understand O(n²) complexity.

## Method Signature

```cs
public static bool HasDuplicatesNaive(int[] numbers)
{
    // Use nested loops to compare every pair of elements
    // Return true if any duplicate is found
}
```

## Expected Results

```cs
HasDuplicatesNaive([1, 2, 3, 4]) -> False
HasDuplicatesNaive([1, 2, 3, 1]) -> True
HasDuplicatesNaive([5, 5]) -> True
```

## Hints

💡 1. The outer loop should iterate from index 0 to numbers.Length - 1

💡 2. The inner loop should start at i + 1 to avoid comparing an element with itself and to skip pairs you've already checked

💡 3. Return true immediately when you find a match - no need to continue checking

💡 4. If the loops complete without finding any duplicates, return false
