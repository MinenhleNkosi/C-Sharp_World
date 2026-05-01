# The Addition Operator

The `+` operator adds two values together. It's one of the most fundamental arithmetic operators in C#.

## Basic Usage

```cs
int sum = 5 + 3;      // sum = 8
int total = 10 + 20;  // total = 30
int result = 0 + 7;   // result = 7
```

## Adding Variables

You can add variables, literals, or a mix of both:

```cs
int a = 15;
int b = 25;
int sum = a + b;      // sum = 40
int mixed = a + 10;   // mixed = 25
```

## Working with Negative Numbers

The addition operator works seamlessly with negative numbers:

```cs
int result1 = 5 + (-3);   // result1 = 2
int result2 = -10 + -5;   // result2 = -15
int result3 = -7 + 7;     // result3 = 0
```

# Visualization

```mermaid
flowchart TD
    A([The Addition Operator in C#]) --> B[What is the + Operator?]
    A --> C[Basic Usage]
    A --> D[Adding Variables]
    A --> E[Working with Negative Numbers]

    B --> B1[Adds two values together]
    B1 --> B2[One of the most fundamental arithmetic operators]

    C --> C1[Add two literals directly]
    C1 --> C2[Example: 5 + 3 = 8]
    C1 --> C3[Example: 10 + 20 = 30]
    C1 --> C4[Example: 0 + 7 = 7]

    D --> D1[Can add variables, literals, or a mix of both]
    D1 --> D2[Variable + Variable]
    D1 --> D3[Variable + Literal]
    D2 --> D2a[Example: a + b where a = 15 and b = 25 = 40]
    D3 --> D3a[Example: a + 10 where a = 15 = 25]

    E --> E1[Works seamlessly with negative numbers]
    E1 --> E2[Positive + Negative]
    E1 --> E3[Negative + Negative]
    E1 --> E4[Negative + Positive - cancel out]
    E2 --> E2a[Example: 5 + -3 = 2]
    E3 --> E3a[Example: -10 + -5 = -15]
    E4 --> E4a[Example: -7 + 7 = 0]
```

The flowchart branches into four sections. **What is the + Operator?** establishes the concept, **Basic Usage** shows literal addition examples, **Adding Variables** covers the three combinations of variables and literals, and **Working with Negative Numbers** maps the three scenarios of mixing positive and negative values.
