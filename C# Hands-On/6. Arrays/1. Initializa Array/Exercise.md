# Your Task

Write a method that prints the first and last elements of an integer array on separate lines. You can use either the traditional approach or the `^` operator.

## Method Signature

```cs
public static void PrintFirstAndLast(int[] numbers)
```

## Expected Output

```cs
PrintFirstAndLast(new int[] { 10, 20, 30, 40 })
// Prints:
// 10
// 40

PrintFirstAndLast(new int[] { 5, 15, 25 })
// Prints:
// 5
// 25
```

## Hints

- Use `numbers[0]` to access the first element
- For the last element, you can use either `numbers[numbers.Length - 1]` or the modern `numbers[^1]` syntax
- Use `Console.WriteLine()` to print each value on its own line

## Example Code

```cs
using System;

public class Solution
{
    public static void PrintFirstAndLast(int[] numbers)
    {
        // Print the first element on one line
        // Print the last element on the next line
    }
}
```
