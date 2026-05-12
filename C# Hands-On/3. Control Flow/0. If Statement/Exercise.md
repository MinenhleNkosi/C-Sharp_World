# Your Task

Write a method that checks if a number is positive (greater than 0). If it is, print the message `The number is positive`. If the number is zero or negative, print nothing.

## Method Signature

```cs
public static void CheckPositive(int number)
```

## Expected Results

```cs
CheckPositive(5)   -> prints "The number is positive"
CheckPositive(100) -> prints "The number is positive"
CheckPositive(0)   -> prints nothing
CheckPositive(-3)  -> prints nothing
```

## Hints

- Use the `>` operator to check if `number` is greater than 0
- The condition goes inside the parentheses: `if (number > 0)`
- Use `Console.WriteLine()` inside the curly braces to print the message
