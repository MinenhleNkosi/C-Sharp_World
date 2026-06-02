# Method Overloading

Method overloading lets you create multiple methods with the same name but different parameters. The compiler determines which method to call based on the arguments you pass.

## Why Use Overloading?

Overloading makes your code more intuitive. Instead of having `AddTwoNumbers()` and `AddThreeNumbers()`, you can simply have `Add()` that works with different numbers of arguments.

## How It Works

```cs
// Two methods with the same name but different parameter counts
public static int Multiply(int a, int b)
{
    return a * b;
}

public static int Multiply(int a, int b, int c)
{
    return a * b * c;
}

// The compiler picks the right one based on arguments
int result1 = Multiply(2, 3);       // Calls first version: 6
int result2 = Multiply(2, 3, 4);    // Calls second version: 24
```

## Overloading Rules

| Valid Difference         | Example                                                  |
| ------------------------ | -------------------------------------------------------- |
| Number of parameters     | `Add(int a, int b)` vs `Add(int a, int b, int c)`        |
| Type of parameters       | `Print(int x)` vs `Print(string x)`                      |
| Order of parameter types | `Process(int a, string b)` vs `Process(string a, int b)` |

**Note**: Return type alone does NOT make methods different enough to overload.

# Visualization

```mermaid
flowchart TD
    A([Method Overloading in C#]) --> B[What is Method Overloading?]
    A --> C[How It Works]
    A --> D[Overloading Rules]
    A --> E[What Does Not Count]

    B --> B1[Multiple methods sharing the same name but with different parameters]
    B1 --> B2[Compiler decides which version to call based on the arguments passed]
    B2 --> B3[Makes code more intuitive - one meaningful name covers multiple use cases]
    B3 --> B4[Replaces Add TwoNumbers and Add ThreeNumbers with a single Add method]

    C --> C1[public static int Multiply int a int b - returns a times b]
    C --> C2[public static int Multiply int a int b int c - returns a times b times c]
    C1 --> C3[Both methods have the same name - differ only in parameter count]
    C2 --> C3
    C3 --> C4[Multiply called with 2 and 3 - compiler picks the two-parameter version]
    C3 --> C5[Multiply called with 2 and 3 and 4 - compiler picks the three-parameter version]
    C4 --> C6[result1 holds 6]
    C5 --> C7[result2 holds 24]
    C6 --> C8[Compiler resolves the correct version at compile time not at runtime]
    C7 --> C8

    D --> D1[Valid difference 1 - number of parameters]
    D --> D2[Valid difference 2 - type of parameters]
    D --> D3[Valid difference 3 - order of parameter types]
    D1 --> D1a[Add int a int b vs Add int a int b int c]
    D1a --> D1b[Different argument counts produce an unambiguous match]
    D2 --> D2a[Print int x vs Print string x]
    D2a --> D2b[Passing an int calls one version - passing a string calls the other]
    D3 --> D3a[Process int a string b vs Process string a int b]
    D3a --> D3b[Argument type order alone is enough to distinguish the two signatures]
    D1b --> D4[Any change to parameter count, type, or order creates a valid overload]
    D2b --> D4
    D3b --> D4

    E --> E1[Return type alone does NOT make a valid overload]
    E1 --> E2[Two methods with the same name and parameters but different return types]
    E2 --> E3[Compiler cannot distinguish them from the call site - no argument difference exists]
    E3 --> E4[Rule: the signature must differ in parameters - return type is not part of the signature]
```

The flowchart branches into four sections. **What is Method Overloading?** establishes the core concept — same name, different parameters — and shows how it replaces a family of awkwardly named methods with a single intuitive one. **How It Works** traces both Multiply versions from definition through to the compiler selecting the correct one at each call site, converging on the point that resolution happens at compile time. **Overloading Rules** maps the three valid forms of difference — parameter count, parameter type, and parameter type order — converging on the rule that any change to the parameter signature is sufficient to create a valid overload. **What Does Not Count** isolates the one thing that is not enough on its own, converging on the rule that return type is not part of the signature the compiler uses to distinguish methods.
