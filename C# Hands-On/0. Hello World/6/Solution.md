# MathConstants.cs file

```cs
/// <summary>
/// Contains mathematical constants used throughout the application.
/// Constants are values that never change during program execution.
/// </summary>
public static class MathConstants
{
    /// <summary>
    /// The mathematical constant PI (π), the ratio of a circle's circumference to its diameter.
    /// </summary>
    public const double Pi = 3.14159;

    /// <summary>
    /// The number of days in a week.
    /// </summary>
    public const int DaysInWeek = 7;

    /// <summary>
    /// The number of hours in a day.
    /// </summary>
    public const int HoursInDay = 24;
}
```

# Main.cs file

```cs
using System;

public class Solution
{
    // Use the constants from MathConstants class

    public static double GetCircleConstant()
    {
        // Return the value of Pi from MathConstants
        return MathConstants.Pi;
    }

    public static int GetDaysInWeek()
    {
        // Return the number of days in a week from MathConstants
        return MathConstants.DaysInWeek;
    }

    public static int GetHoursInDay()
    {
        // Return the number of hours in a day from MathConstants
        return MathConstants.HoursInDay;
    }
}
```
