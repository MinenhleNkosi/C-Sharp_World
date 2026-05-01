```cs

using System;

public class Solution
{
    // Post-increment: returns the original value, then increments
    public static int PostIncrement(int value)
    {
        // Use value++ and return the result
        return value++;
    }

    // Pre-increment: increments first, then returns the new value
    public static int PreIncrement(int value)
    {
        // Use ++value and return the result
        return ++value;
    }

    // Post-decrement: returns the original value, then decrements
    public static int PostDecrement(int value)
    {
        // Use value-- and return the result
        return value--;
    }

    // Pre-decrement: decrements first, then returns the new value
    public static int PreDecrement(int value)
    {
        // Use --value and return the result
        return --value;
    }
}

```
