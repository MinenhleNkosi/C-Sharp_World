```cs
using System;

public class Solution
{
    public static void PrintSkippingMultiplesOfThree()
    {
        // Print numbers 1 to 10, but skip multiples of 3
        // Use the continue statement to skip iterations

        for (int i = 1; i <= 10; i++)
        {
            if (i % 3 == 0)
            {
                continue;
            }

            Console.WriteLine(i);
        }
    }
}
```
