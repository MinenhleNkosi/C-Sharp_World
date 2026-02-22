# Your Task

Write a method that counts and compares operation counts for both complexity classes:

- Count operations in a single loop from `0` to `n-1`
- Count operations in nested loops, each from `0` to `n-1`
- Return both counts as an array `[linearCount, quadraticCount]`

## Method Signature

```cs
public static int[] CompareOperationCounts(int n)
{
    // Your code here
}
```

## Expected Results

```cs
CompareOperationCounts(5) -> [5, 25]
CompareOperationCounts(10) -> [10, 100]
CompareOperationCounts(3) -> [3, 9]
```

## Hints

💡 1. Use two separate counter variables: one for linear operations, one for quadratic operations.

💡 2. For the linear count, increment inside a single `for` loop that runs from `0` to `n-1`.

💡 3. For the quadratic count, increment inside nested loops where both outer and inner loop run from `0` to `n-1`.

💡 4. The quadratic count will always equal `n * n` because the inner loop runs `n` times for each of the `n` outer iterations.
