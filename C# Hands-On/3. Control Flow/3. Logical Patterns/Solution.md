```cs
using System;

public class Solution
{
    public static string ClassifyNumber(int number)
    {
        // Your code here
        var answer = number switch
        {
          0 or 1 => "edge",
          >= 2 and <= 9 => "small positive",
          < 0 => "non-positive",
          >= 10 and <= 100 => "medium",
          _ => "large"
        };

        return answer;
    }
}
```
