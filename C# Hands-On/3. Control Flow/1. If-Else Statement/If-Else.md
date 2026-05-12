# If-Else Statements

The `if-else` statement extends `if` by providing an alternative block of code when the condition is false.

## Basic Structure

```cs
if (condition)
{
    // Runs when condition is true
}
else
{
    // Runs when condition is false
}
```

## If vs If-Else

With just `if`, code after the block always runs. With `if-else`, exactly one block executes:

```cs
// Only if - no alternative action
if (temperature > 30)
{
    Console.WriteLine("It's hot!");
}

// If-else - always takes one path
if (temperature > 30)
{
    Console.WriteLine("It's hot!");
}
else
{
    Console.WriteLine("It's not hot.");
}
```

## The Modulo Operator

The `%` operator returns the remainder after division. It's perfect for checking divisibility:

| Expression | Result | Explanation             |
| ---------- | ------ | ----------------------- |
| `10 % 2`   | 0      | 10 ÷ 2 = 5, remainder 0 |
| `7 % 2`    | 1      | 7 ÷ 2 = 3, remainder 1  |
| `15 % 3`   | 0      | 15 ÷ 3 = 5, remainder 0 |

A number is **even** if `number % 2 == 0`, and **odd** otherwise.

# Visualization

```mermaid
flowchart TD
    A([If-Else Statements in C#]) --> B[What is an If-Else Statement?]
    A --> C[Basic Structure]
    A --> D[If vs If-Else]
    A --> E[The Modulo Operator]

    B --> B1[Extends if by providing an alternative block]
    B1 --> B2[Runs one block when condition is true]
    B2 --> B3[Runs another block when condition is false]
    B3 --> B4[Exactly one block always executes]

    C --> C1[Start with if and a condition in parentheses]
    C1 --> C2{Is condition true?}
    C2 --> |Yes| C3[Run the if block]
    C2 --> |No| C4[Run the else block]
    C3 --> C5[Continue rest of program]
    C4 --> C5

    D --> D1[Only if - no alternative]
    D --> D2[If-else - always takes one path]
    D1 --> D1a{temperature > 30?}
    D1a --> |Yes| D1b[Prints: Its hot!]
    D1a --> |No| D1c[Nothing prints - code after block runs]
    D2 --> D2a{temperature > 30?}
    D2a --> |Yes| D2b[Prints: Its hot!]
    D2a --> |No| D2c[Prints: Its not hot]
    D1c --> D3[If-else guarantees one path always executes]
    D2b --> D3
    D2c --> D3

    E --> E1[% returns the remainder after division]
    E1 --> E2[10 % 2 = 0 - 10 divided by 2 remainder 0]
    E1 --> E3[7 % 2 = 1 - 7 divided by 2 remainder 1]
    E1 --> E4[15 % 3 = 0 - 15 divided by 3 remainder 0]
    E --> E5{number % 2 == 0?}
    E5 --> |Yes - remainder is 0| E6[Number is even]
    E5 --> |No - remainder is 1| E7[Number is odd]
```

The flowchart branches into four sections. **What is an If-Else Statement?** establishes the concept, **Basic Structure** traces the decision point showing both the true and false paths converging back together, **If vs If-Else** contrasts the two approaches highlighting how if-else guarantees one path always runs, and **The Modulo Operator** covers the remainder examples and the even/odd decision logic.
