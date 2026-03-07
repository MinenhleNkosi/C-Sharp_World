# Your Task

Implement a method that uses the `var` keyword to double a value.

Take an `int value`, use `var` to store the value multiplied by 2, and return the result.

## Method Signature

```cs
public static int DoubleValue(int value)
```

## Expected Results

```cs
DoubleValue(5) -> 10
DoubleValue(0) -> 0
DoubleValue(-7) -> -14
```

## Hints

💡 1. Use `var` instead of `int` when declaring your variable, like `var doubled = value * 2;`

💡 2. The `var` keyword still creates a strongly-typed variable - the compiler figures out it's an `int` from the math operation

💡 3. You can return the `var` variable directly since it holds the result
