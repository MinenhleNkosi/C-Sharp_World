# Your Task

Implement a method that checks if a person can access restricted content. A person can access if:

- They are 18 years old or older, **OR**
- They have explicit permission (regardless of age)

Return true if either condition is met, false otherwise.

## Method Signature

```cs
public static bool CheckCondition(int age, bool hasPermission)
```

## Expected Results

```cs
CheckCondition(20, false) -> True   // Adult, no permission needed
CheckCondition(15, true) -> True    // Minor but has permission
CheckCondition(15, false) -> False  // Minor without permission
CheckCondition(18, false) -> True   // Exactly 18, no permission needed
```

## Hints

- The `||` operator returns `true` if the left side OR the right side (or both) is true
- Check if `age >= 18` is true OR if `hasPermission` is true
- You only need a single return statement using the `||` operator
