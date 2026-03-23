# Your Task

Create a method that determines if a person is eligible to vote. A person can vote if they are **an adult** AND they **are a citizen**. Both conditions are provided as boolean parameters.

## Method Signature

```cs
public static bool IsEligibleToVote(bool isAdult, bool isCitizen)
```

## Expected Results

```cs
IsEligibleToVote(true, true) -> True // Adult citizen
IsEligibleToVote(false, true) -> False // Not an adult
IsEligibleToVote(true, false) -> False // Not a citizen
```

## Hints

💡 1. Use the `&&` operator to require both conditions to be true

💡 2. Both `isAdult` and `isCitizen` must be `true` for the result to be `true`

💡 3. You can return the result of combining the two booleans directly
