```cs
using System;

public class Solution
{
    public static string GetLetterGrade(int score)
    {
        // Your code here
        if (score >= 90)
        {
            return "A";
        }
        else if (score >= 80 && score < 90)
        {
            return "B";
        }
        else if (score >= 70 && score < 80)
        {
            return "C";
        }
        else if (score >= 60 && score < 70)
        {
            return "D";
        }
        else
        {
            return "F";
        }
    }
}
```
