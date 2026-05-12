# Your Task

Write a method that categorizes a person based on their age. Return `"Adult"` if the age is 18 or older, otherwise return `"Minor"`. Use the ternary operator to keep your solution concise.

## Method Signature

```cs
public static string GetAgeCategory(int age)
```

## Expected Results

```cs
GetAgeCategory(21) -> "Adult"
GetAgeCategory(10) -> "Minor"
GetAgeCategory(18) -> "Adult"
```

## Hints

- The ternary syntax is: `condition ? trueValue : falseValue`
- Check if `age >= 18` as your condition
- You can return the ternary expression directly without storing it in a variable first
