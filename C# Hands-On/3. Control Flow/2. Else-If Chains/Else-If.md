# Else-If Chains

When you need to check multiple conditions in sequence, use an else-if chain. Only one block executes—the first condition that evaluates to `true`.

## Basic Structure

```cs
if (condition1)
{
    // Runs if condition1 is true
}
else if (condition2)
{
    // Runs if condition1 is false AND condition2 is true
}
else if (condition3)
{
    // Runs if both above are false AND condition3 is true
}
else
{
    // Runs if ALL conditions above are false
}
```

## Order Matters!

Conditions are checked from top to bottom. The first `true` condition wins.

```cs
int temperature = 85;

// WRONG ORDER - always returns "warm" for hot days
if (temperature > 60)
{
    return "warm";  // 85 > 60 is true, stops here!
}
else if (temperature > 80)
{
    return "hot";   // Never reached for 85
}

// CORRECT ORDER - check strictest condition first
if (temperature > 80)
{
    return "hot";   // 85 > 80 is true
}
else if (temperature > 60)
{
    return "warm";
}
```

# Visualization

```mermaid
flowchart TD
    A([Else-If Chains in C#]) --> B[What Are Else-If Chains?]
    A --> C[Basic Structure]
    A --> D[Order Matters]

    B --> B1[Check multiple conditions in sequence]
    B1 --> B2[Only ONE block executes]
    B2 --> B3[The first condition that is true wins]
    B3 --> B4[Remaining conditions are skipped]

    C --> C1[Start with if - first condition]
    C1 --> C2{Is condition1 true?}
    C2 --> |Yes| C3[Run block 1 - skip everything else]
    C2 --> |No| C4{Is condition2 true?}
    C4 --> |Yes| C5[Run block 2 - skip everything else]
    C4 --> |No| C6{Is condition3 true?}
    C6 --> |Yes| C7[Run block 3 - skip everything else]
    C6 --> |No| C8[Run else block - fallback]

    D --> D1[Wrong order example]
    D --> D2[Correct order example]
    D1 --> D1a[temperature = 85]
    D1a --> D1b{temperature > 60?}
    D1b --> |Yes - 85 > 60 is true| D1c[Returns warm - stops here]
    D1c --> D1d[hot block is never reached]
    D2 --> D2a[temperature = 85]
    D2a --> D2b{temperature > 80?}
    D2b --> |Yes - 85 > 80 is true| D2c[Returns hot - correct result]
    D2b --> |No| D2d{temperature > 60?}
    D2d --> |Yes| D2e[Returns warm]
    D1d --> D3[Always check strictest condition first]
    D2c --> D3
```

The flowchart branches into three sections. **What Are Else-If Chains?** establishes the key rule that only one block runs, **Basic Structure** traces the full decision chain from top to bottom showing how each condition falls through to the next, and **Order Matters** contrasts the wrong and correct ordering side by side, both converging on the critical takeaway of checking the strictest condition first.
