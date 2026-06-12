# Your Task

Write a method that modifies an array and prints all its elements:

1. Change the second element (index 1) to the value `99`
2. Print each element of the array on its own line

## Method Signature

```cs
public static void ModifyAndPrint(int[] numbers)
```

## Expected Results

```cs
ModifyAndPrint({10, 20, 30}) prints:
10
99
30

ModifyAndPrint({5, 15}) prints:
5
99
```

## Hints

- Remember that array indices start at 0, so the second element is at index `1`
- Use `numbers[1] = 99;` to change the second element
- Use a `for` loop to iterate through all elements and print each with `Console.WriteLine()`

## Example Code

```cs
using System;

public class Solution
{
    public static void ModifyAndPrint(int[] numbers)
    {
        // Change the second element to 99
        // Then print the modified array
        // Your code here
    }
}
```
