```cs
using System;

public class Solution
{
    public static void ModifyAndPrint(int[] numbers)
    {
        // Change the second element to 99
        // Then print the modified array
        // Your code here
        numbers[1] = 99;
        foreach (int number in numbers)
        {
            Console.WriteLine(number);
        }
    }
}
```
