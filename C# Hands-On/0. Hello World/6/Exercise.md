# Your Task

The `MathConstants.cs` file contains three useful constants. Your task is to access and return each constant value using the class name:

- **GetCircleConstant**: Return the value of `MathConstants.Pi`
- **GetDaysInWeek**: Return the value of `MathConstants.DaysInWeek`
- **GetHoursInDay**: Return the value of `MathConstants.HoursInDay`

Check the `MathConstants.cs` file (click the tab) to see the available constants.

## Method Signatures

```cs
public static double GetCircleConstant()
public static int GetDaysInWeek()
public static int GetHoursInDay()
```

## Expected Results

```cs
GetCircleConstant() -> 3.14159
GetDaysInWeek() -> 7
GetHoursInDay() -> 24
```

## Hints

💡 1. Check the `MathConstants.cs` file to see what constants are available - you'll find `Pi`, `DaysInWeek`, and `HoursInDay`

💡 2. Access static members using `ClassName.MemberName` syntax - for example: `MathConstants.Pi`

💡 3. Simply return the constant value directly using `return MathConstants.ConstantName;`
