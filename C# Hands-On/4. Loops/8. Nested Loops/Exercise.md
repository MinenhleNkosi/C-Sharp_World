# Your Task

Create a 3x3 multiplication table using nested loops. The outer loop represents the row number (1 to 3), and the inner loop represents the column number (1 to 3).

For each cell, print `row * column`. Separate values in a row with a space, and print each row on a new line.

## Method Signature

```cs
public static void PrintMultiplicationTable()
```

## Expected Output

```
1 2 3
2 4 6
3 6 9
```

Row 1: 1×1=1, 1×2=2, 1×3=3 Row 2: 2×1=2, 2×2=4, 2×3=6 Row 3: 3×1=3, 3×2=6, 3×3=9

## Hints

- Use two `for` loops - the outer loop for rows (1 to 3) and the inner loop for columns (1 to 3)
- Use `Console.Write()` to print values on the same line, and `Console.WriteLine()` after the inner loop to move to the next row
- The product at each position is `row * column` - multiply the outer loop variable by the inner loop variable

## Code Format example

```cs
using System;

public class Solution
{
    public static void PrintMultiplicationTable()
    {
        // Your code here
        // Print a 3x3 multiplication table
        // Each row should show: row * 1, row * 2, row * 3
        // Values separated by spaces, each row on a new line
    }
}
```
