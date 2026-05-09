# Your Task

Implement six methods, each using a different comparison operator:

- `IsEqual(a, b)` - return true if a equals b using `==`
- `IsNotEqual(a, b)` - return true if a does not equal b using `!=`
- `IsGreaterThan(a, b)` - return true if a is greater than b using `>`
- `IsLessThan(a, b)` - return true if a is less than b using `<`
- `IsGreaterOrEqual(a, b)` - return true if a is greater than or equal to b using `>=`
- `IsLessOrEqual(a, b)` - return true if a is less than or equal to b using `<=`

## Method Signatures

```cs
public static bool IsEqual(int a, int b)
public static bool IsNotEqual(int a, int b)
public static bool IsGreaterThan(int a, int b)
public static bool IsLessThan(int a, int b)
public static bool IsGreaterOrEqual(int a, int b)
public static bool IsLessOrEqual(int a, int b)
```

## Expected Results

```cs
IsEqual(5, 5) -> True
IsNotEqual(5, 3) -> True
IsGreaterThan(10, 5) -> True
IsLessThan(3, 7) -> True
IsGreaterOrEqual(8, 5) -> True
IsLessOrEqual(4, 9) -> True
```

## Hints

- Use `==` for equality comparison - remember, single `=` is assignment, double `==` is comparison
- The `>=` and `<=` operators return `true` when the values are equal - that's the 'or equal' part
- Each method should be a single return statement using the appropriate comparison operator
