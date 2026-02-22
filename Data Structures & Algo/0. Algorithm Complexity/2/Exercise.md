# Your Task

Implement `HasDuplicatesOptimized` that returns `true` if the array contains any duplicate values, using a HashSet for **O(n)** time complexity.

Important: Use the `HashSet.Add()` method to detect duplicates. Do not use LINQ methods.

## Method Signature

```cs
public static bool HasDuplicatesOptimized(int[] numbers)
{
    // Your code here
}
```

## Expected Results

```cs
HasDuplicatesOptimized([1, 2, 3, 2]) -> True
HasDuplicatesOptimized([1, 2, 3, 4]) -> False
HasDuplicatesOptimized([5, 5]) -> True
```

## Hints

💡 1. Create a HashSet<int> to track numbers you've already seen

💡 2. The Add method returns false if the element already exists in the set

💡 3. Loop through the array once - if Add ever returns false, you found a duplicate
