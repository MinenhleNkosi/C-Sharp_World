# Your Task

Create a method that calculates the distance from the origin (0, 0) to a given point using an `in` parameter.

**Distance Formula**: `√(x² + y²)`

## Method Signature

```cs
public static double DistanceFromOrigin(in Point point)
```

## Expected Results

```cs
DistanceFromOrigin(new Point(3, 4)) -> 5.0
DistanceFromOrigin(new Point(0, 5)) -> 5.0
DistanceFromOrigin(new Point(1, 1)) -> 1.41 (approximately)
```

## Hints

- Use `Math.Sqrt()` to calculate the square root
- The distance formula is `Math.Sqrt(point.X * point.X + point.Y * point.Y)`
- Remember: with `in`, you can read `point.X` and `point.Y` but cannot modify them

## Example Code

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
        // Calculate the distance from origin (0, 0) to the point
        // Use the formula: sqrt(x² + y²)
        // The 'in' keyword means you cannot modify point.X or point.Y
    }
}
```
