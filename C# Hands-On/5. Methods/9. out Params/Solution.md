```cs
using System;

public class Solution
{
    public static bool Divide(int dividend, int divisor, out int quotient, out int remainder)
    {
        // Use out parameters to return both the quotient and remainder
        // Return true if division was successful, false if divisor is zero
        // Hint: Use the helper method DivisionHelper.FormatResult to test your outputs

        // Check for division by zero
        if (divisor == 0)
        {
            quotient = 0;
            remainder = 0;
            return false;
        }

        // Perform integer division and modulo
        quotient = dividend / divisor;
        remainder = dividend % divisor;

        return true;
    }

    // This wrapper method is used for testing - do not modify
    public static string DivideAndFormat(int dividend, int divisor)
    {
        bool success = Divide(dividend, divisor, out int quotient, out int remainder);
        return DivisionHelper.FormatResult(success, quotient, remainder);
    }
}
```
