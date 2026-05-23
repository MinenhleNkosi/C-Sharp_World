```cs
using System;

public class Solution
{
    public static void PrintMultiplicationTable()
    {
        // Print a 3x3 multiplication table
        // No trailing spaces at the end of each line

        for (int row = 1; row <= 3; row++)
        {
            for (int col = 1; col <= 3; col++)
            {
                Console.Write(row * col);

                // Add a space only if it's not the last column
                if (col < 3)
                {
                    Console.Write(" ");
                }
            }

            Console.WriteLine();
        }
    }
}
```
