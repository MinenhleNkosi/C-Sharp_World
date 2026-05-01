# Your Task

Write a method that calculates `(a + b) * c`. You must use parentheses to ensure addition happens before multiplication.

## Method Signature

```cs
public static int Calculate(int a, int b, int c)
```

## Expected Results

```cs
Calculate(2, 3, 4) -> 20
Calculate(5, 5, 2) -> 20
Calculate(0, 10, 5) -> 50
```

## Hints

- Without parentheses, `a + b * c` would multiply `b * c` first due to operator precedence
- Use parentheses `(a + b)` to force the addition to happen before multiplication
- The formula is: first add `a` and `b`, then multiply that sum by `c`
