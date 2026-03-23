```cs
using System;

public class Solution
{
    public static bool IsEligibleToVote(bool isAdult, bool isCitizen)
    {
        // Your code here
        var result = isAdult & isCitizen ? true : false;
        return result;
    }
}
```
