```cs
using System;

public class Solution
{
    public static void PrintUserProfile(string name, int age, double height, decimal balance)
    {
        // Use string interpolation to print a formatted user profile
        // Print exactly 4 lines as shown in the expected results
        Console.WriteLine($"Name: {name}");
        Console.WriteLine($"Age: {age} years old");
        Console.WriteLine($"Height: {height}m");
        Console.WriteLine($"Balance: ${balance}");
    }
}
```
