# Your Task

Write a method that uses a `foreach` loop to print each name in the array on its own line.

## Method Signature

```cs
public static void PrintNames(string[] names)
```

## Expected Output

```cs
PrintNames(["Alice", "Bob", "Charlie"]) prints:
Alice
Bob
Charlie
```

## Hints

- The foreach syntax is: `foreach (string name in names)`
- Use `Console.WriteLine(name)` inside the loop to print each name
- The loop automatically handles empty arrays - it simply doesn't execute the body

## Example Code

```cs
using System;

public class Solution
{
    public static void PrintNames(string[] names)
    {
        // Use foreach to print each name on its own line
    }
}
```
