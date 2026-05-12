# Your Task

Write a method that classifies an integer based on these rules using pattern matching where appropriate:

- Return `"edge"` if the number is 0 or 1 (use `is` with `or`)
- Return `"small positive"` if the number is between 2 and 9 inclusive (use `is` with `and`)
- Return `"non-positive"` if the number is not greater than 0 (use `is` with `not`)
- Return `"medium"` if the number is between 10 and 100 inclusive
- Return `"large"` for all other numbers

## Method Signature

```cs
public static string ClassifyNumber(int number)
```

## Expected Results

```cs
ClassifyNumber(0) -> "edge"
ClassifyNumber(1) -> "edge"
ClassifyNumber(5) -> "small positive"
ClassifyNumber(-5) -> "non-positive"
ClassifyNumber(50) -> "medium"
ClassifyNumber(200) -> "large"
```

## Hints

- Use `number is 0 or 1` to check if a number equals the compile-time constant values 0 or 1
- For a range like 2-9, use `number is > 1 and < 10` - the boundaries 1 and 10 are compile-time constants
- Remember to check conditions in the right order - the edge case (0 or 1) must be checked before the small positive range
