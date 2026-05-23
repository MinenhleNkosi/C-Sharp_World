```cs
using System;

public class Solution
{
    public static void FixInfiniteLoop()
    {
        // This loop is broken - it runs forever!
        // Fix it so it counts from 1 to 5 and then stops

        int counter = 1;

        while (counter <= 5)
        {
            Console.WriteLine(counter);
            // Something is missing here...
            counter++;
        }
    }
}
```
