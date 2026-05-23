# For Loops

A `for` loop is used when you know exactly how many times you want to iterate. It combines initialization, condition, and iteration into a single line.

## For Loop Syntax

```cs
for (initializer; condition; iterator)
{
    // code to execute each iteration
}
```

Three parts:

- **Initializer**: Runs once before the loop starts (e.g., `int i = 0`)
- **Condition**: Checked before each iteration; loop continues while `true`
- **Iterator**: Runs after each iteration (e.g., `i++`)

## Examples

```cs
// Print 0 to 4
for (int i = 0; i < 5; i++)
{
    Console.WriteLine(i);
}

// Print 5 to 1 (counting down)
for (int i = 5; i >= 1; i--)
{
    Console.WriteLine(i);
}

// Print even numbers 2 to 10
for (int i = 2; i <= 10; i += 2)
{
    Console.WriteLine(i);
}
```

## For Loop vs While Loop

| For Loop                                             | While Loop                              |
| ---------------------------------------------------- | --------------------------------------- |
| Best when iteration count is known                   | Best when iteration count is unknown    |
| Initialization, condition, and iterator in one place | These are separate                      |
| `for (int i = 0; i < 5; i++)`                        | `int i = 0; while (i < 5) { ... i++; }` |

# Visualization

```mermaid
flowchart TD
    A([For Loops in C#]) --> B[What is a For Loop?]
    A --> C[Syntax and Structure]
    A --> D[Examples]
    A --> E[For Loop vs While Loop]

    B --> B1[Used when you know exactly how many times to iterate]
    B1 --> B2[Combines initialization, condition, and iterator in one line]
    B2 --> B3[Keeps all loop control logic in a single place]
    B3 --> B4[Preferred over while when iteration count is fixed]

    C --> C1[Structure: for - initializer - condition - iterator - code block]
    C1 --> C2[Initializer - runs once before loop starts - int i = 0]
    C1 --> C3[Condition - checked before each iteration - i < 5]
    C1 --> C4[Iterator - runs after each iteration - i++]
    C2 --> C5[Execute body]
    C3 --> C5
    C4 --> C5
    C5 --> C6{Is condition true?}
    C6 --> |Yes| C7[Run body then run iterator]
    C6 --> |No| C8[Exit loop]
    C7 --> C6

    D --> D1[Count up - print 0 to 4]
    D --> D2[Count down - print 5 to 1]
    D --> D3[Step by 2 - print even numbers 2 to 10]
    D1 --> D1a[int i = 0 - i < 5 - i++]
    D1a --> D1b[Prints 0 1 2 3 4]
    D2 --> D2a[int i = 5 - i >= 1 - i--]
    D2a --> D2b[Prints 5 4 3 2 1]
    D3 --> D3a[int i = 2 - i <= 10 - i += 2]
    D3a --> D3b[Prints 2 4 6 8 10]
    D1b --> D4[Iterator controls both direction and step size]
    D2b --> D4
    D3b --> D4

    E --> E1[Use For Loop when...]
    E --> E2[Use While Loop when...]
    E1 --> E1a[Iteration count is known in advance]
    E1 --> E1b[Init, condition, and iterator belong together]
    E1 --> E1c[Example: for int i = 0 - i < 5 - i++]
    E2 --> E2a[Iteration count depends on runtime conditions]
    E2 --> E2b[Init and update logic are complex or separate]
    E2 --> E2c[Example: int i = 0 - while i < 5 - i++ inside body]
    E1c --> E3[For is more compact but while is more flexible]
    E2c --> E3
```

The flowchart branches into four sections. **What is a For Loop?** establishes when to reach for it — any time the iteration count is known — and highlights that all control logic lives in one line. **Syntax and Structure** breaks down the three header parts in order, then traces execution showing how the condition gates each pass and the iterator fires after every body run. **Examples** maps three common patterns — counting up, counting down, and stepping by two — converging on the insight that the iterator alone controls both direction and step size. **For Loop vs While Loop** contrasts both approaches side by side, converging on the rule that for is the compact choice for fixed counts while while handles open-ended or runtime-driven iteration.
