# Switch Statements

A switch statement is a cleaner alternative to long else-if chains when comparing a single value against multiple constants.

## Basic Syntax

```cs
switch (expression)
{
    case value1:
        // code for value1
        break;
    case value2:
        // code for value2
        break;
    default:
        // code if no case matches
        break;
}
```

## Switch vs Else-If

Switch is preferred when checking one variable against many constant values:

```cs
// Else-if chain (verbose)
if (grade == 'A')
    result = "Excellent";
else if (grade == 'B')
    result = "Good";
else if (grade == 'C')
    result = "Average";
else
    result = "Unknown";

// Switch (cleaner)
switch (grade)
{
    case 'A': result = "Excellent"; break;
    case 'B': result = "Good"; break;
    case 'C': result = "Average"; break;
    default: result = "Unknown"; break;
}
```

## Key Components

| Component | Purpose                  | Required?           |
| --------- | ------------------------ | ------------------- |
| `case`    | Defines a value to match | Yes (at least one)  |
| `break`   | Exits the switch block   | Yes (or return)     |
| `default` | Handles unmatched values | No, but recommended |

## Using Return Instead of Break

When inside a method, you can return directly from a case:

```cs
switch (status)
{
    case 1: return "Active";
    case 2: return "Inactive";
    default: return "Unknown";
}
```

# Visualization

```mermaid
flowchart TD
    A([Switch Statements in C#]) --> B[What is a Switch Statement?]
    A --> C[Basic Syntax]
    A --> D[Switch vs Else-If]
    A --> E[Key Components]
    A --> F[Using Return Instead of Break]

    B --> B1[Cleaner alternative to long else-if chains]
    B1 --> B2[Compares a single value against multiple constants]
    B2 --> B3[More readable when checking many possible values]

    C --> C1[Start with switch and expression in parentheses]
    C1 --> C2{Does expression match a case value?}
    C2 --> |Matches case value1| C3[Run code for value1 then break]
    C2 --> |Matches case value2| C4[Run code for value2 then break]
    C2 --> |No match found| C5[Run default block then break]
    C3 --> C6[Exit switch block]
    C4 --> C6
    C5 --> C6

    D --> D1[Else-if chain - verbose]
    D --> D2[Switch - cleaner]
    D1 --> D1a[if grade == A - Excellent]
    D1 --> D1b[else if grade == B - Good]
    D1 --> D1c[else if grade == C - Average]
    D1 --> D1d[else - Unknown]
    D2 --> D2a[case A: Excellent - break]
    D2 --> D2b[case B: Good - break]
    D2 --> D2c[case C: Average - break]
    D2 --> D2d[default: Unknown - break]
    D1d --> D3[Both produce identical results - switch is preferred]
    D2d --> D3

    E --> E1[case - defines a value to match - required]
    E --> E2[break - exits the switch block - required]
    E --> E3[default - handles unmatched values - recommended]
    E1 --> E1a[At least one case is required]
    E2 --> E2a[Every case needs break or return]
    E3 --> E3a[Not required but handles unexpected values]

    F --> F1[Inside a method you can return directly from a case]
    F1 --> F2[No break needed when using return]
    F2 --> F3[case 1: return Active]
    F2 --> F4[case 2: return Inactive]
    F2 --> F5[default: return Unknown]
    F3 --> F6[Method exits immediately on return]
    F4 --> F6
    F5 --> F6
```

The flowchart branches into five sections. **What is a Switch Statement?** establishes the concept, **Basic Syntax** traces the decision flow through case matching down to the exit point, **Switch vs Else-If** contrasts both approaches converging on the same results, **Key Components** maps each component to its purpose and whether it is required, and **Using Return Instead of Break** shows how returning directly from a case exits the method immediately.
