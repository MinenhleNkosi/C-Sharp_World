# Constants in C#

A constant is a value that cannot change after it's defined. Use the `const` keyword to declare values that remain fixed throughout your program.

## Declaring Constants

```cs
const double SpeedOfLight = 299792458.0;
const int MaxRetries = 3;
const string AppName = "MyApplication";
```

## Constants vs Variables

| Feature          | Constant (`const`)     | Variable             |
| ---------------- | ---------------------- | -------------------- |
| Can change       | No                     | Yes                  |
| Must be assigned | At declaration         | Can be later         |
| Compile-time     | Value known at compile | Value can be runtime |

```cs
const int MaxScore = 100;    // Cannot change
int currentScore = 0;         // Can change
currentScore = 50;            // OK
// MaxScore = 200;            // ERROR: Cannot assign to const
```

## Naming Conventions

C# constants typically use **PascalCase**:

```cs
const double Pi = 3.14159;
const int DaysInWeek = 7;
const string DefaultGreeting = "Hello";
```

## Accessing Static Members from Another Class

When constants (or any static members) are defined in a separate class, you access them using the **class name** followed by a **dot** and the **member name**. This is called **dot notation**.

```cs
// In MathConstants class:
public static class MathConstants
{
  public const double Pi = 3.14159;
  public const int DaysInWeek = 7;
}

// To use these constants from another class:
double circleConstant = MathConstants.Pi; // Returns 3.14159
int days = MathConstants.DaysInWeek; // Returns 7
```

**Why does this work?**

- The `const` keyword makes the value a **static member** of the class (constants are implicitly static).
- Static members belong to the **class itself**, not to any instance.
- You access static members using `ClassName.MemberName` syntax.

```cs
// This pattern applies to all static members:
int result = Math.Max(5, 10); // Built-in Math class
string text = String.Empty; // Built-in String class
double pi = MathConstants.Pi; // Our custom class
```

## Visualization

```mermaid
flowchart TD
    A([Constants in C#]) --> B[Declaring Constants]
    A --> C[Constants vs Variables]
    A --> D[Naming Conventions]
    A --> E[Accessing Static Members from Another Class]

    B --> B1[Use the const keyword]
    B1 --> B2[Value cannot change after definition]
    B2 --> B3[Example: const double SpeedOfLight = 299792458.0]
    B2 --> B4[Example: const int MaxRetries = 3]
    B2 --> B5[Example: const string AppName = MyApplication]

    C --> C1[Constants]
    C --> C2[Variables]
    C1 --> C1a[Cannot change after declaration]
    C1 --> C1b[Must be assigned at declaration]
    C1 --> C1c[Value known at compile time]
    C2 --> C2a[Can change at any time]
    C2 --> C2b[Can be assigned later]
    C2 --> C2c[Value can be determined at runtime]
    C1a --> C3{Attempt to reassign const?}
    C3 --> |Yes| C4[Compiler error]
    C3 --> |No| C5[Valid - value remains fixed]

    D --> D1[Use PascalCase for constant names]
    D1 --> D2[Example: const double Pi = 3.14159]
    D1 --> D3[Example: const int DaysInWeek = 7]
    D1 --> D4[Example: const string DefaultGreeting = Hello]

    E --> E1[Use dot notation - ClassName.MemberName]
    E1 --> E2[Why it works]
    E2 --> E3[const is implicitly static]
    E2 --> E4[Static members belong to the class itself not an instance]
    E2 --> E5[Access using ClassName.MemberName syntax]
    E3 --> E6[Examples]
    E4 --> E6
    E5 --> E6
    E6 --> E6a[MathConstants.Pi returns 3.14159]
    E6 --> E6b[Math.Max-5, 10- built-in class]
    E6 --> E6c[String.Empty built-in class]
```
