# Your Task

Create a `Divide` method that performs integer division and returns both the quotient and remainder using `out` parameters.

- Return `true` if division is successful
- Return `false` if the divisor is zero (avoid division by zero)
- When divisor is zero, set both quotient and remainder to 0
- Check the `DivisionHelper.cs` file for a helper method to format results

## Method Signature

```cs
public static bool Divide(int dividend, int divisor, out int quotient, out int remainder)
```

## Expected Results

```cs
Divide(10, 3, out q, out r) -> true, q=3, r=1
Divide(17, 5, out q, out r) -> true, q=3, r=2
Divide(10, 0, out q, out r) -> false, q=0, r=0
```

## Hints

- Remember that `out` parameters MUST be assigned a value before the method returns, even in error cases
- Use the `/` operator for integer division (quotient) and `%` for the modulo operation (remainder)
- Check if the divisor is zero first, and if so, assign 0 to both `out` parameters before returning `false`
- The `DivisionHelper.FormatResult` method in the helper file shows how your outputs will be formatted for testing

## Example Code

```cs
using System;

public class Solution
{
    public static bool Divide(int dividend, int divisor, out int quotient, out int remainder)
    {
        // Use out parameters to return both the quotient and remainder
        // Return true if division was successful, false if divisor is zero
        // Hint: Use the helper method DivisionHelper.FormatResult to test your outputs
    }

    // This wrapper method is used for testing - do not modify
    public static string DivideAndFormat(int dividend, int divisor)
    {
        bool success = Divide(dividend, divisor, out int quotient, out int remainder);
        return DivisionHelper.FormatResult(success, quotient, remainder);
    }
}
```
