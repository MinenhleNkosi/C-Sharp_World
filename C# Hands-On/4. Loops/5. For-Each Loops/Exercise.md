# Your Task

Write a method that takes an array of fruit names and prints each fruit on a separate line using a `foreach` loop.

## Method Signature

```cs
public static void PrintFruits(string[] fruits)
```

## Expected Results

```cs
PrintFruits(new string[] { "Apple", "Banana", "Cherry" }) prints:
Apple
Banana
Cherry

PrintFruits(new string[] { "Mango" }) prints:
Mango
```

## Hints

- An array like `string[] fruits` holds multiple strings - you receive this as the method parameter
- Use `foreach (string fruit in fruits)` to iterate over each element in the array
- Inside the loop, use `Console.WriteLine(fruit)` to print each fruit on its own line

## Code Format Example

```cs
using System;

public class Solution
{
    public static void PrintFruits(string[] fruits)
    {
        // Use a foreach loop to print each fruit on a new line
    }
}
```
