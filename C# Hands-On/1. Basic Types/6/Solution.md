```cs
using System;

public class Solution
{
    public static void PrintConcatenation(string firstName, string lastName, int age)
    {
        // Use the + operator to concatenate strings
        // Remember: numbers must be converted to strings or concatenated with strings
        // Print three lines:
        // 1. Full name (firstName + space + lastName)
        // 2. A greeting with the name
        // 3. A message with the age

        Console.WriteLine(firstName + " " + lastName);
        Console.WriteLine("Hello, " + firstName + " " + lastName + "!");
        Console.WriteLine(firstName + " " + lastName + " is " + age + " years old.");

    }
}
```
