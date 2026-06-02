```cs
using System;

public struct Point
{
    public double X;
    public double Y;

    public Point(double x, double y)
    {
        X = x;
        Y = y;
    }
}

public class Solution
{
    public static double DistanceFromOrigin(in Point point)
    {
        // Calculate the distance from origin (0, 0)
        return Math.Sqrt(point.X * point.X + point.Y * point.Y);
    }
}
```
