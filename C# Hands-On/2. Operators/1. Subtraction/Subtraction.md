# The Subtraction Operator

The subtraction operator (`-`) calculates the difference between two numbers. It subtracts the right operand from the left operand.

## Basic Usage

```cs
int result = 10 - 3;    // result is 7
int diff = 100 - 45;    // diff is 55
int negative = 5 - 10;  // negative is -5
```

## Subtraction vs Addition

While addition combines values, subtraction finds the difference:

```cs
int sum = 8 + 3;        // 11 (combining)
int difference = 8 - 3; // 5 (finding difference)
```

## Working with Negative Numbers

Subtraction can produce negative results and works with negative operands:

```cs
int result1 = 3 - 10;     // -7 (positive minus larger positive)
int result2 = -5 - 3;     // -8 (negative minus positive)
int result3 = -5 - (-3);  // -2 (subtracting negative adds)
```

# Visualization

```mermaid
flowchart TD
    A([The Subtraction Operator in C#]) --> B[What is the - Operator?]
    A --> C[Basic Usage]
    A --> D[Subtraction vs Addition]
    A --> E[Working with Negative Numbers]

    B --> B1[Calculates the difference between two numbers]
    B1 --> B2[Subtracts the right operand from the left operand]

    C --> C1[Example: 10 - 3 = 7]
    C --> C2[Example: 100 - 45 = 55]
    C --> C3[Example: 5 - 10 = -5 - result can be negative]

    D --> D1[Addition - combines values]
    D --> D2[Subtraction - finds the difference]
    D1 --> D1a[Example: 8 + 3 = 11]
    D2 --> D2a[Example: 8 - 3 = 5]

    E --> E1[Positive minus larger positive]
    E --> E2[Negative minus positive]
    E --> E3[Subtracting a negative adds]
    E1 --> E1a[Example: 3 - 10 = -7]
    E2 --> E2a[Example: -5 - 3 = -8]
    E3 --> E3a[Example: -5 - -3 = -2]
    E3 --> E3b[Subtracting a negative is the same as adding]
```

The flowchart branches into four sections. **What is the - Operator?** establishes the definition, **Basic Usage** shows three examples including a negative result, **Subtraction vs Addition** contrasts the two operators side by side, and **Working with Negative Numbers** covers the three scenarios of mixing positive and negative operands including the important rule that subtracting a negative adds.
