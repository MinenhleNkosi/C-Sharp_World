# If Statements

An `if` statement lets you execute code only when a condition is true. It's the foundation of decision-making in programming.

## Basic Syntax

```cs
if (condition)
{
    // Code runs only when condition is true
}
```

The condition must evaluate to a `bool` (true or false). The curly braces `{ }` define the code block that executes.

# Comparison Operators

Use these operators to create conditions:

| Operator | Meaning               | Example          |
| -------- | --------------------- | ---------------- |
| `>`      | Greater than          | `5 > 3` is true  |
| `<`      | Less than             | `2 < 7` is true  |
| `>=`     | Greater than or equal | `5 >= 5` is true |
| `<=`     | Less than or equal    | `3 <= 4` is true |
| `==`     | Equal to              | `5 == 5` is true |
| `!=`     | Not equal to          | `5 != 3` is true |

## Examples

```cs
int age = 18;
if (age >= 18)
{
    Console.WriteLine("You are an adult");
}

int temperature = 30;
if (temperature > 25)
{
    Console.WriteLine("It's hot outside");
}
```

# Visualization

```mermaid
flowchart TD
    A([If Statements in C#]) --> B[What is an If Statement?]
    A --> C[Basic Syntax]
    A --> D[Comparison Operators]
    A --> E[Examples]

    B --> B1[Executes code only when a condition is true]
    B1 --> B2[Foundation of decision-making in programming]
    B2 --> B3[Condition must evaluate to a boolean - true or false]

    C --> C1[Start with the if keyword]
    C1 --> C2[Condition goes inside parentheses]
    C2 --> C3[Code block goes inside curly braces]
    C3 --> C4{Is condition true?}
    C4 --> |Yes| C5[Code block executes]
    C4 --> |No| C6[Code block is skipped]

    D --> D1[> Greater than - 5 > 3 is true]
    D --> D2[< Less than - 2 < 7 is true]
    D --> D3[>= Greater than or equal - 5 >= 5 is true]
    D --> D4[<= Less than or equal - 3 <= 4 is true]
    D --> D5[== Equal to - 5 == 5 is true]
    D --> D6[!= Not equal to - 5 != 3 is true]

    E --> E1[Age check example]
    E --> E2[Temperature check example]
    E1 --> E1a[int age = 18]
    E1a --> E1b{age >= 18?}
    E1b --> |Yes| E1c[Prints: You are an adult]
    E1b --> |No| E1d[Nothing prints]
    E2 --> E2a[int temperature = 30]
    E2a --> E2b{temperature > 25?}
    E2b --> |Yes| E2c[Prints: Its hot outside]
    E2b --> |No| E2d[Nothing prints]
```

The flowchart branches into four sections. **What is an If Statement?** establishes the concept, **Basic Syntax** traces the structure through to the decision point showing both the true and false paths, **Comparison Operators** maps all six operators with their meanings and examples, and **Examples** walks through both the age and temperature checks as decision trees showing what happens in each case.
