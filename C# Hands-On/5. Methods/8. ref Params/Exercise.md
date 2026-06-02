# Your Task

1. Implement the `Swap` method that exchanges two integers using `ref`
2. In `SwapAndReturn`, call your `Swap` method with the correct `ref` syntax
3. Return the result using `ResultFormatter.Format(a, b)`

## Method Signatures

- `public static void Swap(ref int x, ref int y)` - Swaps the values
- `public static string SwapAndReturn(int a, int b)` - Calls Swap and returns formatted result

## Expected Results

```cs
SwapAndReturn(5, 10) -> "a=10, b=5"
SwapAndReturn(1, 2) -> "a=2, b=1"
```

## Hints

- Use a temporary variable to hold one value while you overwrite it: `int temp = x;`
- When calling a method with `ref` parameters, you must use the `ref` keyword at the call site: `Swap(ref a, ref b)`
- The swap pattern is: save first value, overwrite first with second, set second to saved value

## Example Code

```cs
using System;

public class Solution
{
    public static string SwapAndReturn(int a, int b)
    {
        // Call the Swap method from SwapHelper to swap the values
        // Then use ResultFormatter.Format to return the result
    }

    // Implement the Swap method that exchanges two integers using ref
    public static void Swap(ref int x, ref int y)
    {
        // Your code here - swap the values of x and y
    }
}
```
