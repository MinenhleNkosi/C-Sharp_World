# Your Task

Write a method that prints "Even" if the number is divisible by 2, or "Odd" if it's not.

## Method Signature

```cs
public static void PrintEvenOrOdd(int number)
```

## Expected Results

```cs
PrintEvenOrOdd(4)  -> prints "Even"
PrintEvenOrOdd(7)  -> prints "Odd"
PrintEvenOrOdd(0)  -> prints "Even"
```

## Hints

- Use the modulo operator `%` to find the remainder when dividing by 2
- If `number % 2 == 0`, the number is even; otherwise, it's odd
- The `else` block handles all cases where the `if` condition is false
