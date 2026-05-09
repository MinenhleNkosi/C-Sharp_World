# Your Task

Create a function that takes a boolean `isBusy` and returns the opposite value. If someone is busy, return `false` (they are NOT available). If someone is NOT busy, return `true` (they ARE available).

## Method Signature

```cs
public static bool IsNotBusy(bool isBusy)
```

## Expected Results

```cs
IsNotBusy(true) -> False
IsNotBusy(false) -> True
```

## Hints

- The `!` operator goes before the boolean value you want to negate
- If `isBusy` is `true`, then `!isBusy` is `false`
- You can return the negated value directly: `return !variableName;`
