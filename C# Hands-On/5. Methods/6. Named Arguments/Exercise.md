# Your Task

Call the `CreateProfile` method using different combinations of named and positional arguments based on the scenario number provided. For any scenario other than 1-4, return `"Invalid scenario"`.

## Method Signature

```cs
public static string CallWithNamedArguments(int scenario)
```

## Expected Results

```cs
CallWithNamedArguments(1) -> "Alice, 25, Paris, True" (all named, reverse order)
CallWithNamedArguments(2) -> "Bob, 30, London, False" (city first)
CallWithNamedArguments(3) -> "Carol, 22, Tokyo, True" (mixed)
CallWithNamedArguments(4) -> "David, 40, Berlin, False" (mostly positional)
CallWithNamedArguments(99) -> "Invalid scenario" (any value not 1-4)
```

## Hints

- Use the syntax `parameterName: value` to specify named arguments
- For scenario 1, all four arguments should be named: `CreateProfile(isActive: true, city: "Paris", ...)`
- When mixing positional and named, positional arguments must come first: `CreateProfile("Carol", 22, city: "Tokyo", isActive: true)`
- Use a `switch` statement with a `default` case to handle invalid scenarios

## Example Code

```cs
using System;

public class Solution
{
    // DO NOT MODIFY THIS METHOD - it's for testing your named argument calls
    public static string CreateProfile(string name, int age, string city, bool isActive)
    {
        return $"{name}, {age}, {city}, {isActive}";
    }

    public static string CallWithNamedArguments(int scenario)
    {
        // Call CreateProfile using named arguments based on the scenario:
        // Scenario 1: Call with arguments in reverse order (isActive, city, age, name)
        //             Values: name="Alice", age=25, city="Paris", isActive=true
        // Scenario 2: Call with city first, then name, age, isActive
        //             Values: name="Bob", age=30, city="London", isActive=false
        // Scenario 3: Mix positional and named - first two positional (name, age), last two named
        //             Values: name="Carol", age=22, city="Tokyo", isActive=true
        // Scenario 4: Call with only isActive named, others positional
        //             Values: name="David", age=40, city="Berlin", isActive=false
        // Any other scenario: Return "Invalid scenario"

        // Your code here
    }
}
```
