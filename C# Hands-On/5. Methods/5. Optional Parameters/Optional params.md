# Optional Parameters

Optional parameters let you define default values for method parameters, making them optional when calling the method.

## Basic Syntax

```cs
// Parameter with default value - must come after required parameters
public static void SayHello(string name, string greeting = "Hello")
{
    Console.WriteLine($"{greeting}, {name}!");
}

// Calling with both arguments
SayHello("Alice", "Hi");  // Output: Hi, Alice!

// Calling with only required argument - uses default
SayHello("Bob");          // Output: Hello, Bob!
```

## Rules for Optional Parameters

```cs
// ✓ Optional parameters must come AFTER required ones
public static void Method(int required, int optional = 10) { }

// ✗ This would NOT compile - optional before required
// public static void Method(int optional = 10, int required) { }

// Multiple optional parameters are allowed
public static double Calculate(double value, double multiplier = 1.0, int precision = 2)
{
    return Math.Round(value * multiplier, precision);
}

Calculate(5.5);              // Uses defaults: multiplier=1.0, precision=2
Calculate(5.5, 2.0);         // Uses multiplier=2
Calculate(5.5, 2.0, 3);      // All arguments provided
```

## Named Arguments with Optionals

```cs
public static string Format(string text, bool uppercase = false, bool addBrackets = false)
{
    var result = uppercase ? text.ToUpper() : text;
    return addBrackets ? $"[{result}]" : result;
}

// Skip middle optional parameter using named argument
Format("hello", addBrackets: true);  // Returns: [hello]
```

# Visualization

```mermaid
flowchart TD
    A([Optional Parameters in C#]) --> B[What are Optional Parameters?]
    A --> C[Basic Syntax]
    A --> D[Rules for Optional Parameters]
    A --> E[Named Arguments with Optionals]

    B --> B1[Parameters with default values defined in the method signature]
    B1 --> B2[Caller can omit them and the default value is used automatically]
    B2 --> B3[Reduces the need to overload methods just to handle missing arguments]
    B3 --> B4[Required parameters and optional parameters can coexist in one signature]

    C --> C1[public static void SayHello string name string greeting = Hello]
    C1 --> C2[name is required - greeting is optional with default value Hello]
    C2 --> C3[SayHello called with Alice and Hi - both arguments provided]
    C2 --> C4[SayHello called with Bob only - greeting falls back to Hello]
    C3 --> C5[Output: Hi Alice]
    C4 --> C6[Output: Hello Bob]
    C5 --> C7[When an argument is supplied it overrides the default]
    C6 --> C7

    D --> D1[Optional parameters must come after all required parameters]
    D --> D2[Multiple optional parameters are allowed in one signature]
    D1 --> D1a[Method int required int optional = 10 - valid ordering]
    D1a --> D1b[Method int optional = 10 int required - does not compile]
    D1b --> D1c[Compiler cannot resolve which argument maps where if optional comes first]
    D2 --> D2a[Calculate double value double multiplier = 1.0 int precision = 2]
    D2a --> D2b[Calculate of 5.5 - both defaults apply - multiplier 1.0 precision 2]
    D2a --> D2c[Calculate of 5.5 and 2.0 - multiplier overridden - precision stays 2]
    D2a --> D2d[Calculate of 5.5 and 2.0 and 3 - all three arguments supplied]
    D1c --> D3[Rule: optional parameters fill from right - required parameters fill from left]
    D2b --> D3
    D2c --> D3
    D2d --> D3

    E --> E1[Named arguments let you target a specific optional parameter by name]
    E1 --> E2[public static string Format string text bool uppercase = false bool addBrackets = false]
    E2 --> E3[Format called with hello and addBrackets true - uppercase skipped entirely]
    E3 --> E4[Named argument jumps over the middle optional without providing it]
    E4 --> E5[Output: hello in brackets]
    E5 --> E6[Rule: named arguments let you skip optional parameters that sit between others]
    E6 --> E7[Combine optional parameters with named arguments for maximum calling flexibility]
```

The flowchart branches into four sections. **What are Optional Parameters?** establishes the concept — default values baked into the signature so the caller can omit them — and shows how they reduce the need for multiple overloads. **Basic Syntax** traces the SayHello method through both calling styles, converging on the rule that a supplied argument always overrides the default. **Rules for Optional Parameters** maps the valid and invalid orderings and walks through all three ways to call the Calculate method, converging on the principle that optional parameters fill from right to left while required parameters must always be satisfied. **Named Arguments with Optionals** shows how naming an argument at the call site lets you jump over an intermediate optional entirely, converging on the guideline that named arguments and optional parameters together give the caller maximum flexibility over which defaults to keep and which to override.
