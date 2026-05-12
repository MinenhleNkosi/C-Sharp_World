# Your Task

Convert a numeric score (0-100) to a letter grade:

| Score Range | Letter Grade |
| ----------- | ------------ |
| 90-100      | A            |
| 80-89       | B            |
| 70-79       | C            |
| 60-69       | D            |
| 0-59        | F            |

## Method Signature

```cs
public static string GetLetterGrade(int score)
```

## Expected Results

```cs
GetLetterGrade(95) -> "A"
GetLetterGrade(82) -> "B"
GetLetterGrade(73) -> "C"
GetLetterGrade(65) -> "D"
GetLetterGrade(45) -> "F"
```

## Hints

- Start by checking the highest grade range first (90 and above for an A)
- Use `>=` to include the boundary value in each range
- The final `else` handles all scores below 60—no condition needed there
