```cs
using System;

public class Solution
{
    public static void PrintCharInfo(char c)
    {
        // Your code here
        // Print the character
        // Print whether it's a letter
        // Print whether it's a digit
        // Print whether it's uppercase
        Console.WriteLine(c);
        Console.WriteLine(char.IsLetter(c));
        Console.WriteLine(char.IsDigit(c));
        Console.WriteLine(char.IsUpper(c));
    }
}
```
