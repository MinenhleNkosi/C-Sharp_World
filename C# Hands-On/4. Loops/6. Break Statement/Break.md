# The break Statement

The `break` statement immediately exits the current loop, stopping all further iterations. Use it when you've found what you're looking for and don't need to continue searching.

## Basic Usage

```cs
for (int i = 1; i <= 10; i++)
{
    if (i == 5)
    {
        break; // Exits the loop when i equals 5
    }
    Console.WriteLine(i);
}
// Prints: 1, 2, 3, 4 (stops before printing 5)
```

## Finding the First Match

```cs
int[] numbers = { 3, 8, 15, 22, 7 };
foreach (int num in numbers)
{
    if (num > 10)
    {
        Console.WriteLine($"First number over 10: {num}");
        break; // Stop searching after finding the first match
    }
}
// Prints: First number over 10: 15
```

## Why Use break?

| Scenario         | Without break    | With break           |
| ---------------- | ---------------- | -------------------- |
| Find first match | Checks all items | Stops at first match |
| Loop iterations  | All 100          | Only until found     |
| Efficiency       | Wastes time      | More efficient       |

## Divisibility Check

To check if a number is divisible by another, use the modulo operator `%`. If `a % b == 0`, then `a` is evenly divisible by `b`.

```cs
14 % 7 == 0  // True - 14 is divisible by 7
15 % 7 == 0  // False - 15 is not divisible by 7
```

# Visualization

```mermaid
flowchart TD
    A([The break Statement in C#]) --> B[What is break?]
    A --> C[Basic Usage]
    A --> D[Finding the First Match]
    A --> E[Why Use break?]
    A --> F[Divisibility Check]

    B --> B1[Immediately exits the current loop]
    B1 --> B2[All remaining iterations are skipped]
    B2 --> B3[Execution continues with the code after the loop]
    B3 --> B4[Use when you have found what you need and searching further is unnecessary]

    C --> C1[for int i = 1 - i <= 10 - i++ with if i == 5 break]
    C1 --> C2[i = 1 to 4 - condition false - prints each value]
    C2 --> C3[i = 5 - if condition true - break fires]
    C3 --> C4[Loop exits immediately - 5 is never printed]
    C4 --> C5[Output: 1 2 3 4 - stops before reaching 5]

    D --> D1[Array: 3 8 15 22 7 - searching for first value over 10]
    D1 --> D2[num = 3 - not over 10 - continue]
    D2 --> D3[num = 8 - not over 10 - continue]
    D3 --> D4[num = 15 - over 10 - print result then break]
    D4 --> D5[Loop exits - 22 and 7 are never checked]
    D5 --> D6[Output: First number over 10: 15]

    E --> E1[Without break]
    E --> E2[With break]
    E1 --> E1a[Every element is checked even after match is found]
    E1a --> E1b[All 100 iterations run regardless of result]
    E1b --> E1c[Wastes time on unnecessary work]
    E2 --> E2a[Loop stops as soon as the first match is found]
    E2a --> E2b[Only iterates until the target is located]
    E2b --> E2c[More efficient for search and find scenarios]
    E1c --> E3[break trades completeness for efficiency - use when first match is enough]
    E2c --> E3

    F --> F1[Modulo operator % returns the remainder after division]
    F1 --> F2[If a % b == 0 then a is evenly divisible by b]
    F2 --> F3[14 % 7 == 0 is true - 14 is divisible by 7]
    F2 --> F4[15 % 7 == 0 is false - 15 is not divisible by 7]
    F3 --> F5[Commonly paired with break to stop on the first divisible match]
    F4 --> F5
```

The flowchart branches into five sections. **What is break?** establishes that break is an immediate exit — remaining iterations are skipped and execution jumps to the code after the loop. **Basic Usage** traces each iteration of the counting example showing exactly which values print and why 5 is never reached. **Finding the First Match** walks through each array element in sequence, showing the loop advancing until the condition hits on 15 and break fires, leaving the remaining elements unchecked. **Why Use break?** contrasts the without and with cases across three dimensions — coverage, iteration count, and efficiency — converging on the rule that break is the right tool when the first match is all you need. **Divisibility Check** introduces the modulo operator, maps a true and false example, and converges on its natural pairing with break for stopping at the first divisible result.
