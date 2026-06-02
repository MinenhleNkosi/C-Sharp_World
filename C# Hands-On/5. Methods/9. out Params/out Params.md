# The out Keyword

The `out` keyword allows a method to return multiple values by passing variables that the method will assign. Unlike `ref`, `out` parameters don't need to be initialized before passing.

## out vs ref

```cs
// ref: variable MUST be initialized before passing
int refVar = 5;
SomeMethod(ref refVar);  // Can read and modify refVar

// out: variable does NOT need initialization
int outVar;
SomeMethod(out outVar);  // Method MUST assign outVar
```

## Key Differences

| Feature                     | ref                   | out                      |
| --------------------------- | --------------------- | ------------------------ |
| Must initialize before call | Yes                   | No                       |
| Method must assign value    | No                    | Yes                      |
| Can read incoming value     | Yes                   | No (undefined)           |
| Purpose                     | Modify existing value | Return additional values |

## Using out Parameters

```cs
// Method with out parameters
public static bool TryParse(string input, out int result)
{
    // out parameter MUST be assigned before returning
    result = 0;  // Assign default

    if (int.TryParse(input, out int parsed))
    {
        result = parsed;
        return true;
    }
    return false;
}

// Calling the method
if (TryParse("42", out int value))
{
    Console.WriteLine(value);  // 42
}
```

## Inline Declaration

C# allows declaring `out` variables inline when calling a method:

```cs
// Old style
int quotient;
int remainder;
Divide(10, 3, out quotient, out remainder);

// Modern inline style
Divide(10, 3, out int quotient, out int remainder);
```

# Visualization

```mermaid
flowchart TD
    A([The out Keyword in C#]) --> B[What is the out Keyword?]
    A --> C[out vs ref]
    A --> D[Using out Parameters]
    A --> E[Inline Declaration]

    B --> B1[Allows a method to return multiple values through its parameters]
    B1 --> B2[Variables passed with out are assigned inside the method not before]
    B2 --> B3[Unlike ref the variable does not need to be initialized before passing]
    B3 --> B4[The method takes on the responsibility of assigning every out parameter]

    C --> C1[ref - variable must be initialized before the call]
    C --> C2[out - variable does not need initialization before the call]
    C1 --> C3[int refVar = 5 - SomeMethod ref refVar - method can read and modify the value]
    C2 --> C4[int outVar declared but not assigned - SomeMethod out outVar - method must assign it]
    C3 --> C5[ref purpose: modify an existing value and pass it in both directions]
    C4 --> C6[out purpose: return one or more additional values from a method]
    C5 --> C7[Key rule: ref is two-way - out is write-only from the method's perspective]
    C6 --> C7

    D --> D1[public static bool TryParse string input out int result]
    D1 --> D2[result must be assigned before any return path is reached]
    D2 --> D3[Assign default value result = 0 at the start to satisfy the compiler]
    D3 --> D4[If int.TryParse succeeds assign parsed to result and return true]
    D3 --> D5[If int.TryParse fails result stays 0 and method returns false]
    D4 --> D6[Caller writes: if TryParse 42 out int value]
    D5 --> D6
    D6 --> D7[When method returns true value holds 42 and is ready to use]
    D7 --> D8[out lets one method communicate both success or failure and the resulting data]

    E --> E1[Old style - declare variable on one line then pass it on the next]
    E --> E2[Modern inline style - declare the variable directly at the call site]
    E1 --> E1a[int quotient declared - int remainder declared - Divide 10 3 out quotient out remainder]
    E1a --> E1b[Two extra lines of declaration before the call adds noise]
    E2 --> E2a[Divide 10 3 out int quotient out int remainder - declaration and call in one line]
    E2a --> E2b[Compiler infers the variable scope from the call site]
    E1b --> E3[Inline declaration reduces boilerplate and keeps the variable close to where it is used]
    E2b --> E3
    E3 --> E4[Rule: prefer inline out declaration unless the variable is needed before the call]
```

The flowchart branches into four sections. **What is the out Keyword?** establishes the core contract — the caller supplies an uninitialized variable and the method takes on the obligation of assigning it before returning. **out vs ref** contrasts the two keywords across initialization requirements, assignment obligations, and read access, converging on the rule that ref is two-way while out is write-only from the method's perspective. **Using out Parameters** walks through the TryParse implementation step by step, tracing both the success and failure paths and converging on the insight that out lets a single method communicate both an outcome and the resulting data simultaneously. **Inline Declaration** contrasts the old two-step style against the modern single-line form, converging on the guideline that inline declaration should be preferred whenever the variable is not needed before the call.
