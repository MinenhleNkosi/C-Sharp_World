# The Ternary Operator

The ternary operator (`?:`) is a compact way to write simple if-else statements in a single expression. Use it when you need to choose between two values based on a condition.

## Syntax

```cs
condition ? valueIfTrue : valueIfFalse
```

The operator evaluates the condition. If true, it returns the first value; if false, it returns the second value.

## Basic Examples

```cs
// Instead of this:
string result;
if (score >= 50)
    result = "Pass";
else
    result = "Fail";

// Write this:
string result = score >= 50 ? "Pass" : "Fail";

// More examples:
int max = a > b ? a : b;
bool isEven = number % 2 == 0 ? true : false;
string greeting = hour < 12 ? "Good morning" : "Good afternoon";
```

## Ternary vs If-Else

| Ternary                 | If-Else                |
| ----------------------- | ---------------------- |
| Returns a value         | Executes statements    |
| Single expression       | Multiple lines         |
| Best for simple choices | Best for complex logic |

```cs
// Ternary - concise for simple assignments
string status = isActive ? "Online" : "Offline";

// If-Else - better for multiple operations
if (isActive)
{
    status = "Online";
    LogActivity();
}
else
{
    status = "Offline";
    SendNotification();
}
```

# Visualization

```mermaid
flowchart TD
    A([The Ternary Operator in C#]) --> B[What is the Ternary Operator?]
    A --> C[Syntax]
    A --> D[Basic Examples]
    A --> E[Ternary vs If-Else]

    B --> B1[Compact way to write simple if-else in one expression]
    B1 --> B2[Uses the ?: symbols]
    B2 --> B3[Evaluates a condition and returns one of two values]

    C --> C1[Structure: condition ? valueIfTrue : valueIfFalse]
    C1 --> C2{Is condition true?}
    C2 --> |Yes| C3[Returns valueIfTrue]
    C2 --> |No| C4[Returns valueIfFalse]
    C3 --> C5[Result assigned to variable]
    C4 --> C5

    D --> D1[Pass or Fail example]
    D --> D2[Max value example]
    D --> D3[Even or odd example]
    D --> D4[Greeting example]
    D1 --> D1a[score >= 50 ? Pass : Fail]
    D1a --> D1b[Replaces 4 line if-else with one line]
    D2 --> D2a[a > b ? a : b - returns the larger value]
    D3 --> D3a[number % 2 == 0 ? true : false]
    D4 --> D4a[hour < 12 ? Good morning : Good afternoon]

    E --> E1[Use Ternary when...]
    E --> E2[Use If-Else when...]
    E1 --> E1a[Returning a single value]
    E1 --> E1b[Simple one-line assignments]
    E1 --> E1c[Example: status = isActive ? Online : Offline]
    E2 --> E2a[Executing multiple statements per branch]
    E2 --> E2b[Complex logic with method calls]
    E2 --> E2c[Example: if isActive - set status AND call LogActivity]
    E1c --> E3[Ternary is concise but limited to simple choices]
    E2c --> E3
```

The flowchart branches into four sections. **What is the Ternary Operator?** establishes the concept, **Syntax** traces the decision flow showing how the condition maps to one of two return values, **Basic Examples** maps four real-world examples showing how each replaces a verbose if-else, and **Ternary vs If-Else** contrasts the two approaches converging on the key rule that ternary suits simple choices while if-else handles complex multi-statement logic.
