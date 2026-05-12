# Your Task

Create a method that converts a day number (1-7) to the corresponding day name using a **switch expression**.

- 1 = "Monday"
- 2 = "Tuesday"
- 3 = "Wednesday"
- 4 = "Thursday"
- 5 = "Friday"
- 6 = "Saturday"
- 7 = "Sunday"
- Any other number = "Invalid day"

## Method Signature

```cs
public static string GetDayName(int dayNumber)
```

## Expected Results

```cs
GetDayName(1) -> "Monday"
GetDayName(5) -> "Friday"
GetDayName(7) -> "Sunday"
GetDayName(0) -> "Invalid day"
```

## Hints

- Use the `switch` keyword followed by the variable and the `switch` keyword pattern: `dayNumber switch { ... }`
- Each case uses `=>` instead of `case:` and `return`. Example: `1 => "Monday"`
- Use the discard pattern `_` to handle invalid day numbers (like `default` in switch statements)
