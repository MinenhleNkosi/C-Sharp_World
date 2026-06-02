# Your Task

Implement a method that calculates the sum of all numbers passed to it using the `params` keyword. The method should handle any number of integer arguments, including zero arguments (which should return 0).

## Method Signature

```cs
public static int SumAll(params int[] numbers)
```

## Expected Results

```cs
SumAll(1, 2, 3) -> 6
SumAll(10) -> 10
SumAll() -> 0
SumAll(5, 5, 5, 5, 5) -> 25
```

## Hints

- The `params int[] numbers` behaves like a regular array inside the method - you can use `foreach` to iterate through it
- When no arguments are passed, `numbers.Length` will be 0 - make sure your code handles this case
- Initialize a sum variable to 0, then add each number to it using a loop

## Example Code

```cs
using System;

public class Solution
{
    public static int SumAll(params int[] numbers)
    {
        // Your code here
    }
}
```
