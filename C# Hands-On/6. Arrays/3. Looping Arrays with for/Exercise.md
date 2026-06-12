# Your Task

Write a method that prints all elements of an integer array, each on its own line, using a `for` loop.

## Method Signature

```cs
public static void PrintAllElements(int[] numbers)
```

## Expected Results

```cs
PrintAllElements([1, 2, 3]) prints:
1
2
3

PrintAllElements([42]) prints:
42
```

## Hints

- Use `numbers.Length` to determine how many times to loop
- Array indices start at 0, so your loop should start with `int i = 0`
- Use `Console.WriteLine(numbers[i])` inside the loop to print each element

## Example Code

```cs
using System;

public class Solution
{
    public static void PrintAllElements(int[] numbers)
    {
        // Use a for loop to print each element on its own line
        // Hint: Use numbers.Length to get the array size
    }
}
```
