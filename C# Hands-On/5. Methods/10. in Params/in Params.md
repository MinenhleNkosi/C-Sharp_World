# The in Keyword

The `in` keyword passes arguments **by reference as read-only**, allowing efficient passing of large value types while guaranteeing the method cannot modify the original value.

## Why Use in Parameters?

```cs
// Without 'in': the struct is copied (expensive for large structs)
public static double Calculate(Point p) { ... }

// With 'in': passed by reference, no copy made
public static double Calculate(in Point p) { ... }
```

## Read-Only Guarantee

Unlike `ref`, the `in` keyword prevents modification:

```cs
public static void Process(in Point p)
{
    // p.X = 10;  // ERROR: Cannot modify - it's read-only!
    double x = p.X;  // OK: Reading is allowed
}
```

## Comparison: ref vs in vs out

| Modifier | Can Read | Can Modify | Must Initialize Before | Must Assign Inside |
| -------- | -------- | ---------- | ---------------------- | ------------------ |
| `ref`    | Yes      | Yes        | Yes                    | No                 |
| `in`     | Yes      | No         | Yes                    | No                 |
| `out`    | Yes      | Yes        | No                     | Yes                |

## When to Use in

- Passing large structs (more than 16 bytes) to avoid copying overhead
- When you want to guarantee the method won't change the value
- For performance-critical code with value types

# Visualization

```mermaid
flowchart TD
    A([The in Keyword in C#]) --> B[What is the in Keyword?]
    A --> C[Read-Only Guarantee]
    A --> D[ref vs in vs out]
    A --> E[When to Use in]

    B --> B1[Passes arguments by reference but as read-only]
    B1 --> B2[No copy of the value is made when the method is called]
    B2 --> B3[The method can read the value but cannot modify the original]
    B3 --> B4[Designed for large value types where copying is expensive]

    C --> C1[Without in - struct is copied entirely when passed to the method]
    C --> C2[With in - struct is passed by reference and no copy is made]
    C1 --> C3[public static double Calculate Point p - Point copied on every call]
    C2 --> C4[public static double Calculate in Point p - reference passed, original untouched]
    C3 --> C5[Copying is invisible to the caller but adds overhead for large structs]
    C4 --> C6[Compiler enforces read-only access - any attempt to modify produces an error]
    C5 --> C7[in gives the performance of ref with the safety guarantee of a read-only value]
    C6 --> C7

    D --> D1[Reading the incoming value]
    D --> D2[Modifying the incoming value]
    D --> D3[Must initialize before the call]
    D --> D4[Must assign inside the method]
    D1 --> D1a[ref - allowed - in - allowed - out - allowed]
    D2 --> D2a[ref - allowed - in - NOT allowed - out - allowed]
    D3 --> D3a[ref - yes required - in - yes required - out - no not required]
    D4 --> D4a[ref - no not required - in - no not required - out - yes required]
    D1a --> D5[ref and out can change the original - in can only observe it]
    D2a --> D5
    D3a --> D5
    D4a --> D5
    D5 --> D6[Rule: use in when you want by-reference efficiency with a read-only contract]

    E --> E1[Large structs exceeding 16 bytes where copying overhead is measurable]
    E --> E2[When the method must guarantee it will not alter the caller's value]
    E --> E3[Performance-critical code working with value types in tight loops]
    E1 --> E1a[Small structs and primitives are cheap to copy - in adds little benefit there]
    E2 --> E2a[in makes the no-modification contract explicit and compiler-enforced]
    E3 --> E3a[Avoiding copies across many iterations compounds into meaningful savings]
    E1a --> E4[in is a precision tool - use it where the cost of copying is real and measurable]
    E2a --> E4
    E3a --> E4
```

The flowchart branches into four sections. **What is the in Keyword?** establishes the dual promise — by-reference passing for efficiency and a read-only contract for safety — positioning it as the tool for large value types where copying overhead matters. **Read-Only Guarantee** contrasts the without-in and with-in forms of the same method, converging on the point that the compiler actively enforces the read-only restriction and any modification attempt produces an error. **ref vs in vs out** maps all three modifiers across the four behavioural dimensions — reading, modifying, pre-call initialization, and post-call assignment — converging on the rule that ref and out can alter the original while in can only observe it. **When to Use in** maps the three conditions that justify reaching for it — large structs, explicit no-modification contracts, and performance-critical loops — converging on the guideline that in is a precision tool whose benefit only materialises where the cost of copying is real.
