# Order of Operations

C# follows mathematical precedence rules (PEMDAS/BODMAS). Multiplication and division execute before addition and subtraction. Parentheses override this default order.

## Default Precedence

```cs
int result1 = 2 + 3 * 4;    // = 2 + 12 = 14 (multiplication first)
int result2 = 10 - 6 / 2;   // = 10 - 3 = 7 (division first)
int result3 = 8 / 4 * 2;    // = 2 * 2 = 4 (left to right for same precedence)
```

## Using Parentheses

Parentheses force operations to happen first, regardless of default precedence.

```cs
int result1 = (2 + 3) * 4;  // = 5 * 4 = 20 (parentheses first)
int result2 = (10 - 6) / 2; // = 4 / 2 = 2 (parentheses first)
int result3 = 10 / (2 + 3); // = 10 / 5 = 2 (parentheses first)
```

## Operator Precedence Table

| Priority | Operators     | Description                      |
| -------- | ------------- | -------------------------------- |
| 1 (High) | `( )`         | Parentheses                      |
| 2        | `*`, `/`, `%` | Multiplication, Division, Modulo |
| 3 (Low)  | `+`, `-`      | Addition, Subtraction            |

```mermaid
flowchart TD
    A([Order of Operations in C#]) --> B[What is Order of Operations?]
    A --> C[Default Precedence]
    A --> D[Using Parentheses]
    A --> E[Operator Precedence Table]

    B --> B1[C# follows PEMDAS and BODMAS rules]
    B1 --> B2[Multiplication and division execute before addition and subtraction]
    B2 --> B3[Parentheses override the default order]

    C --> C1[Multiplication first]
    C --> C2[Division first]
    C --> C3[Same precedence - left to right]
    C1 --> C1a[Example: 2 + 3 * 4]
    C1a --> C1b[3 * 4 = 12 first then 2 + 12 = 14]
    C2 --> C2a[Example: 10 - 6 / 2]
    C2a --> C2b[6 / 2 = 3 first then 10 - 3 = 7]
    C3 --> C3a[Example: 8 / 4 * 2]
    C3a --> C3b[8 / 4 = 2 first then 2 * 2 = 4]

    D --> D1[Parentheses force operations to happen first]
    D1 --> D2[Example: 2 + 3 * 4]
    D1 --> D3[Example: 10 - 6 / 2]
    D1 --> D4[Example: 10 / 2 + 3]
    D2 --> D2a[Without parentheses: 2 + 3 * 4 = 14]
    D2 --> D2b[With parentheses: 2 + 3 * 4 = 20]
    D3 --> D3a[Without parentheses: 10 - 6 / 2 = 7]
    D3 --> D3b[With parentheses: 10 - 6 / 2 = 2]
    D4 --> D4a[With parentheses: 10 / 2 + 3 = 2]

    E --> E1[Priority 1 - Highest: Parentheses]
    E --> E2[Priority 2: Multiplication, Division, Modulo]
    E --> E3[Priority 3 - Lowest: Addition, Subtraction]
    E1 --> E4[Evaluated first regardless of position]
    E2 --> E5[Evaluated before addition and subtraction]
    E3 --> E6[Evaluated last]
```

The flowchart branches into four sections. **What is Order of Operations?** establishes the PEMDAS rules, **Default Precedence** traces three examples showing how multiplication, division, and same-level operators are evaluated, **Using Parentheses** contrasts results with and without parentheses for each example, and **Operator Precedence Table** maps the three priority levels from highest to lowest.
