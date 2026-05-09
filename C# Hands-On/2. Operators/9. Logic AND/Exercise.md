# Your Task

Write a method that determines if a person can enter an amusement park. A person can enter if:

1. They are at least 5 years old (age >= 5), **AND**
2. They have a ticket (hasTicket is true)

Both conditions must be true for entry to be allowed.

## Method Signature

```cs
public static bool CanEnterPark(int age, bool hasTicket)
```

## Expected Results

```cs
CanEnterPark(10, true) -> True
CanEnterPark(10, false) -> False
CanEnterPark(3, true) -> False
CanEnterPark(5, true) -> True
```

## Hints

- Use the `&&` operator to combine the two conditions
- The age check uses the `>=` comparison operator: `age >= 5`
- The ticket check is already a boolean, so you can use `hasTicket` directly in the condition
