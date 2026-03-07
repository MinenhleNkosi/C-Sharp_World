# Multi-Line Comments

Multi-line comments let you write comments that span multiple lines. Use them to explain complex logic, or temporarily disable blocks of code.

## Syntax

```cs
/* This is a
   multi-line comment.
   It can span many lines. */
```

## Single-Line vs Multi-Line Comments

```cs
// Single line - good for brief notes
int x = 5; // Also works at end of line

/* Multi-line comments are ideal for:
   - Explaining algorithms
   - Temporarily disabling code blocks */
```

Common Uses
| Use Case | Example |
|---|---|
| Method docs | `/* Calculates total price */` |
| Parameters | `/* a - first value, b - second */` |
| Disable code | `/* Console.WriteLine("debug"); */` |

## The Return Keyword

The `return` keyword does two things:

- **Exits the method immediately** - no code after return runs
- **Sends a value back to the caller** - the value becomes the result of the method call

```cs
public static int Double(int x)
{
    return x * 2;  // Sends back the doubled value
}

int result = Double(5);  // result is now 10
```

The type after `return` must match the method's return type (e.g., `int` methods must return an `int`).

## Visualization

```mermaid
flowchart TD
    A([Multi-Line Comments and Return Keyword]) --> B[Multi-Line Comments]
    A --> C[Single-Line vs Multi-Line]
    A --> D[Common Uses]
    A --> E[The Return Keyword]

    B --> B1[Spans multiple lines]
    B1 --> B2[Opens with /*]
    B2 --> B3[Closes with */]
    B3 --> B4[Everything between is ignored by the compiler]

    C --> C1[Single-Line //]
    C --> C2[Multi-Line /* */]
    C1 --> C1a[Good for brief notes]
    C1 --> C1b[Can appear at end of a line]
    C2 --> C2a[Ideal for explaining algorithms]
    C2 --> C2b[Good for disabling blocks of code]

    D --> D1[Method documentation]
    D --> D2[Parameter descriptions]
    D --> D3[Disable code blocks temporarily]
    D1 --> D1a[Example: /* Calculates total price */]
    D2 --> D2a[Example: /* a - first value, b - second */]
    D3 --> D3a[Example: /* Console.WriteLine - debug - */]

    E --> E1[Exits the method immediately]
    E --> E2[Sends a value back to the caller]
    E1 --> E3[No code after return runs]
    E2 --> E4[Value becomes the result of the method call]
    E4 --> E5{Return type matches method type?}
    E5 --> |Yes - int method returns int| E6[Valid - compiles successfully]
    E5 --> |No - type mismatch| E7[Invalid - compiler error]
    E6 --> E8[Example: return x * 2 inside int Double-int x-]
```
