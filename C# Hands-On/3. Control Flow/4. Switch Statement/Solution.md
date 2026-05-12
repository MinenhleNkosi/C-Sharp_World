```cs
using System;

public class Solution
{
    public static string GetDayName(int dayNumber)
    {
        // Your code here
        var dayResult = dayNumber switch
        {
          1 => "Monday",
          2 => "Tuesday",
          3 => "Wednesday",
          4 => "Thursday",
          5 => "Friday",
          6 => "Saturday",
          7 => "Sunday",
          _ => "Invalid day"
        };

        return dayResult;
    }
}
```
