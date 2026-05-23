```cs
using System;

public class Solution
{
    public static void DisplayMenu()
    {
        // Create a do-while loop that:
        // 1. Displays the menu header
        // 2. Displays menu options
        // 3. Displays a counter value
        // 4. Continues while counter is less than 3

        // Menu format:
        // === MENU ===
        // 1. Exit
        // 2. Say Hello
        // 3. Say Goodbye
        // Iteration: [number]

        // Your code here
        int number = 1;
        do
        {
            Console.WriteLine("=== MENU ===");
            Console.WriteLine("1. Exit");
            Console.WriteLine("2. Say Hello");
            Console.WriteLine("3. Say Goodbye");
            Console.WriteLine($"Iteration: {number}");
            number++;
        }while (number <= 3);
    }
}
```
