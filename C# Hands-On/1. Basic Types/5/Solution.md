```cs
using System;

public class Solution
{
    public static void PrintFilePaths()
    {
        // Print a Windows file path using verbatim string
        // Path: C:\Users\Admin\Documents\report.txt
        Console.WriteLine(@"C:\Users\Admin\Documents\report.txt");

        // Print a multi-line SQL query using verbatim string
        // SELECT *
        // FROM Users
        // WHERE Active = 1

        // Your code here
        Console.WriteLine(@"SELECT *");
        Console.WriteLine(@"FROM Users");
        Console.WriteLine(@"WHERE Active = 1");
    }
}
```
