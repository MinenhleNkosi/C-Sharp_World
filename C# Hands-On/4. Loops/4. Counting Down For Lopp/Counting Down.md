# For Loops - Counting Down

A for loop can count in any direction by changing the loop variable's increment/decrement operation. Counting down is useful for countdowns, reverse iteration, and scenarios where you need to process items from last to first.

## Decrementing with `i--`

```cs
// Count up: start low, end high, increment
for (int i = 1; i <= 5; i++)
{
    Console.WriteLine(i);  // Prints: 1, 2, 3, 4, 5
}

// Count down: start high, end low, decrement
for (int i = 5; i >= 1; i--)
{
    Console.WriteLine(i);  // Prints: 5, 4, 3, 2, 1
}
```

## Key Differences from Counting Up

| Counting Up            | Counting Down         |
| ---------------------- | --------------------- |
| Start at smaller value | Start at larger value |
| Condition: `i <= max`  | Condition: `i >= min` |
| Increment: `i++`       | Decrement: `i--`      |

## Decrement Variations

```cs
// Decrement by 1
for (int i = 10; i >= 1; i--)

// Decrement by 2 (even numbers backwards)
for (int i = 10; i >= 2; i -= 2)  // 10, 8, 6, 4, 2

// Decrement by custom amount
for (int i = 100; i >= 0; i -= 10)  // 100, 90, 80, ..., 0
```

# Visualization

```mermaid
flowchart TD
    A([For Loops - Counting Down in C#]) --> B[What is Counting Down?]
    A --> C[Key Differences from Counting Up]
    A --> D[Count Up vs Count Down]
    A --> E[Decrement Variations]

    B --> B1[Change direction by adjusting the iterator operation]
    B1 --> B2[Start at a high value and decrement each iteration]
    B2 --> B3[Useful for countdowns, reverse iteration, last-to-first processing]
    B3 --> B4[Same for loop structure - only initializer, condition, and iterator change]

    C --> C1[Counting up - start low, condition checks max, increment with i++]
    C --> C2[Counting down - start high, condition checks min, decrement with i--]
    C1 --> C3[Initializer sets the starting bound]
    C2 --> C3
    C3 --> C4[Condition must match direction - <= for up, >= for down]
    C4 --> C5[Iterator must move toward the exit condition or loop runs forever]

    D --> D1[Count up example]
    D --> D2[Count down example]
    D1 --> D1a[int i = 1 - i <= 5 - i++]
    D1a --> D1b[Prints 1 2 3 4 5]
    D2 --> D2a[int i = 5 - i >= 1 - i--]
    D2a --> D2b[Prints 5 4 3 2 1]
    D1b --> D3[Both loops cover the same range in opposite directions]
    D2b --> D3

    E --> E1[Decrement by 1]
    E --> E2[Decrement by 2]
    E --> E3[Decrement by custom amount]
    E1 --> E1a[int i = 10 - i >= 1 - i--]
    E1a --> E1b[Prints 10 9 8 7 6 5 4 3 2 1]
    E2 --> E2a[int i = 10 - i >= 2 - i -= 2]
    E2a --> E2b[Prints 10 8 6 4 2]
    E3 --> E3a[int i = 100 - i >= 0 - i -= 10]
    E3a --> E3b[Prints 100 90 80 70 60 50 40 30 20 10 0]
    E1b --> E4[Step size in i -= n controls how many values are skipped each pass]
    E2b --> E4
    E3b --> E4
```

The flowchart branches into four sections. **What is Counting Down?** establishes that direction is controlled entirely by the iterator and that the overall loop structure stays the same. **Key Differences from Counting Up** contrasts the three header parts side by side, converging on two rules — the condition operator must match the direction and the iterator must always move toward making the condition false. **Count Up vs Count Down** pairs the two canonical examples over the same range to make the mirror relationship concrete. **Decrement Variations** maps decrement by 1, by 2, and by a custom step, converging on the insight that the value of n in `i -= n` determines how many values are skipped each pass.
