# Your Task

Implement `ComplexityCapstone` that returns an array with three values:

- **hasDuplicateNaive**: 1 if duplicates found using nested loops, 0 otherwise.
- **hasDuplicateHashSet**: 1 if duplicates found using HashSet, 0 otherwise.
- **binarySearchStepsForMiddle**: Number of comparisons to find the middle element of the sorted array using binary search.

For the binary search:

- Sort a copy of the input array.
- Find the middle value: `sorted[length / 2]`
- Count how many comparisons binary search needs to find it

If the array is empty, return `[0, 0, 0]`.

**Important**: You must implement all algorithms manually - no built-in shortcuts for duplicate detection, searching, or summation.

## Method Signature

```cs
public static int[] ComplexityCapstone(int[] numbers)
```

## Expected Results

```cs
ComplexityCapstone([1, 2, 3, 4, 5]) -> [0, 0, 1]
ComplexityCapstone([1, 2, 2, 4, 5]) -> [1, 1, 1]
ComplexityCapstone([]) -> [0, 0, 0]
```

## Hints

💡 1. For the naive check, use two nested loops where `j` starts at `i + 1` to compare each pair exactly once.

💡 2. Use `HashSet<int>.Add()` which returns `false` if the element already exists - this gives you `O(1)` duplicate detection.

💡 3. Remember to sort a copy of the array before binary search, and use sorted `[sorted.Length / 2]` as your target.

💡 4. Count each comparison in binary search by incrementing a counter inside the `while` loop before checking the condition.
