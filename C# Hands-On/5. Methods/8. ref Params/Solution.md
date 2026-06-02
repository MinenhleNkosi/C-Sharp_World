```cs
using System;

public class Solution
{
    public static string SwapAndReturn(int a, int b)
    {
        // Call the Swap method from SwapHelper to swap the values
        // Then use ResultFormatter.Format to return the result
        SwapHelper.DemoSwap(ref a , ref b);
        return ResultFormatter.Format(a, b);
    }

    // Implement the Swap method that exchanges two integers using ref
    public static void Swap(ref int x, ref int y)
    {
        // Your code here - swap the values of x and y
        int z = x;
        x = y;
        y = z;
    }
}
```
