# Switch Expressions

Switch expressions are a concise, expression-based alternative to switch statements. They return a value directly and use the `=>` arrow syntax.

## Basic Syntax

```cs
// Switch expression syntax
var result = value switch
{
    pattern1 => result1,
    pattern2 => result2,
    _ => defaultResult  // discard pattern (default)
};
```

## Switch Statement vs Switch Expression

```cs
// Traditional switch statement (verbose)
string GetGrade(int score)
{
    switch (score)
    {
        case 10:
            return "A+";
        case 9:
            return "A";
        default:
            return "B";
    }
}

// Switch expression (concise)
string GetGrade(int score) => score switch
{
    10 => "A+",
    9 => "A",
    _ => "B"
};
```

## Key Differences

| Feature        | Switch Statement | Switch Expression |
| -------------- | ---------------- | ----------------- |
| Returns value  | Via `return`     | Directly          |
| Uses `case:`   | Yes              | No, uses `=>`     |
| Uses `break`   | Yes              | No                |
| Default        | `default:`       | `_` (discard)     |
| Exhaustiveness | Optional         | Required          |

## The Discard Pattern `_`

The underscore `_` is the discard pattern - it matches anything not matched by previous patterns. It's equivalent to `default` in switch statements.

# Visualization

```mermaid
flowchart TD
    A([Switch Expressions in C#]) --> B[What is a Switch Expression?]
    A --> C[Basic Syntax]
    A --> D[Switch Statement vs Switch Expression]
    A --> E[Key Differences]
    A --> F[The Discard Pattern]

    B --> B1[Concise expression-based alternative to switch statements]
    B1 --> B2[Returns a value directly]
    B2 --> B3[Uses the => arrow syntax instead of case and break]

    C --> C1[Value followed by switch keyword]
    C1 --> C2[Each arm uses => to map pattern to result]
    C2 --> C3{Does value match a pattern?}
    C3 --> |Matches pattern1| C4[Returns result1]
    C3 --> |Matches pattern2| C5[Returns result2]
    C3 --> |No match| C6[Returns default via discard pattern _]
    C4 --> C7[Result assigned to variable]
    C5 --> C7
    C6 --> C7

    D --> D1[Switch statement - verbose]
    D --> D2[Switch expression - concise]
    D1 --> D1a[switch score with case blocks]
    D1a --> D1b[case 10: return A+]
    D1a --> D1c[case 9: return A]
    D1a --> D1d[default: return B]
    D2 --> D2a[score switch with arrow arms]
    D2a --> D2b[10 => A+]
    D2a --> D2c[9 => A]
    D2a --> D2d[_ => B]
    D1d --> D3[Both produce identical results - expression is more concise]
    D2d --> D3

    E --> E1[Returns value: statement uses return - expression returns directly]
    E --> E2[Syntax: statement uses case: - expression uses =>]
    E --> E3[Break: required in statement - not used in expression]
    E --> E4[Default: statement uses default: - expression uses _ discard]
    E --> E5[Exhaustiveness: optional in statement - required in expression]

    F --> F1[The underscore _ is the discard pattern]
    F1 --> F2[Matches anything not matched by previous patterns]
    F2 --> F3[Equivalent to default in switch statements]
    F3 --> F4[Required in switch expressions for exhaustiveness]
```

The flowchart branches into five sections. **What is a Switch Expression?** establishes the concept, **Basic Syntax** traces the pattern matching decision flow down to the result assignment, **Switch Statement vs Switch Expression** contrasts both approaches side by side converging on the same output, **Key Differences** maps the five feature distinctions between the two forms, and **The Discard Pattern** explains the role and requirement of the underscore as a catch-all.
