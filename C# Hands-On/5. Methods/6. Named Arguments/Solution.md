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
        string answer = scenario switch
        {
            1 => CreateProfile(isActive: true, city: "Paris", age: 25, name: "Alice"),
            2 => CreateProfile(city: "London", name: "Bob", age: 30, isActive: false),
            3 => CreateProfile("Carol", 22, city: "Tokyo", isActive: true),
            4 => CreateProfile("David", 40, "Berlin", isActive: false),
            _ => "Invalid scenario"
        };

        return answer;
    }
}
```
