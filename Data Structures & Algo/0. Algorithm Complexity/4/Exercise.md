# Your Task

Implement binary search that **counts and returns the number of comparison steps**. Each time you compare the middle element to the target counts as one step - whether you find the target or not.

**Important**: You must implement the binary search algorithm manually. Built-in search methods are not allowed for this exercise.

## Method Signature

```cs
public static int CountBinarySearchSteps(int[] sortedArray, int target)
{
    // Implement binary search and count each comparison
    // Return the total number of steps (comparisons) made
}
```

## Expected Results

```cs
CountBinarySearchSteps([1, 3, 5, 7, 9], 5) -> 1  // Middle element is target
CountBinarySearchSteps([1, 3, 5, 7, 9], 9) -> 3  // Check 5, then 7, then 9
CountBinarySearchSteps([1, 3, 5, 7, 9], 4) -> 3  // Not found after 3 steps
```

## Hints

💡 1. Use left and right pointers to track the current search range, and a steps counter

💡 2. Calculate the middle index as mid = left + (right - left) / 2 to avoid integer overflow

💡 3. Increment the step counter each time you compare sortedArray[mid] to target

💡 4. Continue the loop while left <= right - when left exceeds right, the element isn't present
