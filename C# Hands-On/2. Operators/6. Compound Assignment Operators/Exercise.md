# Your Task

Implement four methods, each using a different compound assignment operator:

- `ApplyAdditionAssignment`: Use `+=` to add amount to value
- `ApplySubtractionAssignment`: Use `-=` to subtract amount from value
- `ApplyMultiplicationAssignment`: Use `*=` to multiply value by amount
- `ApplyDivisionAssignment`: Use `/=` to divide value by amount

## Method Signatures

```cs
public static int ApplyAdditionAssignment(int value, int amount)
public static int ApplySubtractionAssignment(int value, int amount)
public static int ApplyMultiplicationAssignment(int value, int amount)
public static int ApplyDivisionAssignment(int value, int amount)
```

## Expected Results

```cs
ApplyAdditionAssignment(10, 5) -> 15
ApplySubtractionAssignment(20, 8) -> 12
ApplyMultiplicationAssignment(7, 3) -> 21
ApplyDivisionAssignment(100, 4) -> 25
```

## Hints

- The `+=` operator is shorthand for `value = value + amount`
- Remember to modify the `value` variable using the compound operator, then return it
- Each compound operator follows the same pattern: `variable op= amount` is equivalent to `variable = variable op amount`
