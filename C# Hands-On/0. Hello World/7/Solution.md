```cs
using System;

public class Solution
{
    public static string DescribeValue(int value)
    {
        // Use var to store the value
        var storeValue = value;
        // Return a message describing what was stored
        return "Stored: " + storeValue;
    }

    public static string DescribeText(string text)
    {
        // Use var to store the text
        var storeText = text;
        // Return a message including the text
        return "Text is: " + storeText;
    }
}
```
