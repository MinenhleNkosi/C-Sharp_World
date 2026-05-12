# Your Task

Write a method that converts a day number (1-7) to its corresponding day name. Use Monday as day 1 through Sunday as day 7. Return "Invalid day" for any number outside this range.

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

- Use `switch (dayNumber)` to begin your switch statement
- Create a `case` for each day number from 1 to 7, returning the appropriate day name
- Use the `default` case to handle any number that isn't 1-7
