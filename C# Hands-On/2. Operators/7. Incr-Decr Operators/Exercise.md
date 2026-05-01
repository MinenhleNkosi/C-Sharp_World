# Your Task

Implement four methods that demonstrate each type of increment/decrement operator:

- `PostIncrement(value)` - Use `value++` and return the result
- `PreIncrement(value)` - Use `++value` and return the result
- `PostDecrement(value)` - Use `value--` and return the result
- `PreDecrement(value)` - Use `--value` and return the result

## Method Signatures

```cs
public static int PostIncrement(int value)
public static int PreIncrement(int value)
public static int PostDecrement(int value)
public static int PreDecrement(int value)
```

## Expected Results

```cs
PostIncrement(5) -> 5   // Returns original value
PreIncrement(5) -> 6    // Returns incremented value
PostDecrement(10) -> 10 // Returns original value
PreDecrement(10) -> 9   // Returns decremented value
```

## Hints

- Remember: `value++` returns the value **before** incrementing, while `++value` returns the value **after** incrementing
- Post-fix operators (`x++`, `x--`) give you the old value; prefix operators (`++x`, `--x`) give you the new value
- Think of it as: **postfix** = 'return first, change later' and **prefix** = 'change first, return later'
