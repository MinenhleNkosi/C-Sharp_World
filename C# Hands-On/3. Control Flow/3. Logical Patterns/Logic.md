# Logical Patterns with `is`, `and`, `or`, `not`

C# pattern matching allows you to combine conditions using pattern combinators. These make your code more readable when comparing against **compile-time constants**.

## Important: Compile-Time Constants Only

Pattern matching with `is` only works with values known at compile time:

```cs
// ✅ Works - 0 and 1 are compile-time constants
if (number is 0 or 1) { }

// ❌ Does NOT compile - variables are not constants
int min = 0;
int max = 10;
if (number is > min and < max) { }  // Error!

// ✅ For variables, use traditional operators
if (number > min && number < max) { }  // Works!
```

## The `or` Pattern Combinator

```cs
// Match if number equals any of these constant values
if (number is 1 or 2 or 3)
{
    Console.WriteLine("One, two, or three");
}

// Works with constant relational patterns
if (number is < 0 or > 100)
{
    Console.WriteLine("Out of range");
}
```

## The `and` Pattern Combinator

```cs
// Match if number is in a range (constant boundaries)
if (number is > 0 and < 10)
{
    Console.WriteLine("Between 1 and 9");
}

// Combine multiple constant conditions
if (number is >= 1 and <= 100 and not 50)
{
    Console.WriteLine("1-100, but not 50");
}
```

## The `not` Pattern Combinator

```cs
// Match if NOT equal to a constant value
if (number is not 0)
{
    Console.WriteLine("Not zero");
}

// Negate a relational pattern
if (number is not > 0)
{
    Console.WriteLine("Zero or negative");
}
```

## When to Use Pattern Matching vs Boolean Operators

| Scenario                            | Use Pattern Matching | Use Boolean Operators   |
| ----------------------------------- | -------------------- | ----------------------- |
| Compare to literals (1, 2, "hello") | ✅ `x is 1 or 2`     | `x == 1 \|\| x == 2`    |
| Compare to const values             | ✅ `x is MyConst`    | `x == MyConst`          |
| Compare to variables                | ❌ Won't compile     | ✅ `x > min && x < max` |
| Dynamic boundaries                  | ❌ Won't compile     | ✅ Use `&&` and `\|\|`  |

# Visualization

```mermaid
flowchart TD
    A([Logical Patterns with is, and, or, not in C#]) --> B[Important: Compile-Time Constants Only]
    A --> C[The or Pattern Combinator]
    A --> D[The and Pattern Combinator]
    A --> E[The not Pattern Combinator]
    A --> F[Pattern Matching vs Boolean Operators]

    B --> B1[Pattern matching with is only works with compile-time constants]
    B1 --> B2{Are values known at compile time?}
    B2 --> |Yes - literals like 0 and 1| B3[Valid - use is with pattern combinators]
    B2 --> |No - variables like min and max| B4[Invalid - will not compile]
    B4 --> B5[Use traditional operators instead - && and double pipe]

    C --> C1[Match if value equals ANY of the listed constants]
    C1 --> C2[Example: number is 1 or 2 or 3]
    C2 --> C2a[Prints: One two or three]
    C1 --> C3[Works with relational patterns too]
    C3 --> C3a[Example: number is less than 0 or greater than 100]
    C3a --> C3b[Prints: Out of range]

    D --> D1[Match if value satisfies ALL conditions]
    D1 --> D2[Example: number is greater than 0 and less than 10]
    D2 --> D2a[Prints: Between 1 and 9]
    D1 --> D3[Can combine multiple constant conditions]
    D3 --> D3a[Example: number is >= 1 and <= 100 and not 50]
    D3a --> D3b[Prints: 1-100 but not 50]

    E --> E1[Match if value does NOT equal the constant]
    E1 --> E2[Example: number is not 0]
    E2 --> E2a[Prints: Not zero]
    E1 --> E3[Can negate relational patterns]
    E3 --> E3a[Example: number is not greater than 0]
    E3a --> E3b[Prints: Zero or negative]

    F --> F1[Use Pattern Matching]
    F --> F2[Use Boolean Operators]
    F1 --> F1a[Comparing to literals - x is 1 or 2]
    F1 --> F1b[Comparing to const values - x is MyConst]
    F2 --> F2a[Comparing to variables - x > min AND x < max]
    F2 --> F2b[Dynamic boundaries - use AND and OR operators]
    F1 --> F3[Pattern matching will not compile with variables]
    F2 --> F4[Boolean operators work in all scenarios]
```

The flowchart branches into five sections. **Compile-Time Constants Only** establishes the key constraint with a decision point between valid and invalid usage, **The or Combinator** covers matching any listed value or relational pattern, **The and Combinator** shows how to match ranges and multiple conditions simultaneously, **The not Combinator** demonstrates negating both equality and relational patterns, and **Pattern Matching vs Boolean Operators** maps the four scenarios to the appropriate approach.
