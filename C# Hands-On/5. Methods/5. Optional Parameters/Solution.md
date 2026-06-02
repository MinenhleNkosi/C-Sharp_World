```cs
using System;

public class Solution
{
    // Implement the Greet method with an optional prefix parameter
    // The prefix should default to "Hello" if not provided
    public static string Greet(string name, string prefix = "Hello")
    {
        return $"{prefix}, {name}!";
    }
}
```
