# Your Task

Define and implement a `Greet` method that returns a personalized greeting. The method should:

- Take a required `name` parameter (string)
- Take an optional `prefix` parameter with a default value of `"Hello"`
- Return the greeting in the format: `"{prefix}, {name}!"`

You need to write the complete method definition including the optional parameter syntax.

## Method Signature

```cs
public static string Greet(string name, string prefix = "Hello")
```

## Expected Results

```cs
Greet("Alice") -> "Hello, Alice!"
Greet("Bob", "Hi") -> "Hi, Bob!"
Greet("World", "Greetings") -> "Greetings, World!"
```

## Hints

- Define the method with two parameters: `string name` (required) and `string prefix = "Hello"` (optional with default)
- Use string interpolation `$"{prefix}, {name}!"` to build the greeting
- Remember that optional parameters must come after required parameters in the method signature

## Example Code

```cs
using System;

public class Solution
{
    // Implement the Greet method with an optional prefix parameter
    // The prefix should default to "Hello" if not provided

}
```
