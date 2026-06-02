# Your Task

1. Create a **private static** method called `PrintGreeting` that prints `Hello, World!` to the console
2. Call `PrintGreeting` from within the `Greet` method

## Method Signatures

```cs
public static void Greet()
private static void PrintGreeting()
```

## Expected Results

```cs
Greet() prints: Hello, World!
```

## Hints

- A private method is defined with `private static void MethodName()`
- Use `Console.WriteLine("text")` inside your private method to print the greeting
- Since both methods are static and in the same class, call your private method simply by using its name: `PrintGreeting();`

## Example Code

```cs
using System;

public class Solution
{
    public static void Greet()
    {
        // Call your private greeting method here
    }

    // Define a private method called PrintGreeting that prints "Hello, World!"
    // Your code here
}
```
