# Multiplication Operator

The multiplication operator `*` multiplies two numbers together. It's used whenever you need to calculate products, areas, or scale values.

## Basic Usage

```cs
int product = 5 * 3;     // product = 15
int doubled = 7 * 2;     // doubled = 14
int scaled = 100 * 10;   // scaled = 1000
```

## Multiplication vs Addition

While addition combines values, multiplication repeats a value a certain number of times:

```cs
// Adding 4 three times
int sum = 4 + 4 + 4;      // sum = 12

// Multiplying is shorter
int product = 4 * 3;      // product = 12
```

## Special Cases

```cs
int zero = 5 * 0;         // Any number times zero = 0
int same = 8 * 1;         // Any number times one = itself (8)
int negative = 4 * -2;    // Positive times negative = negative (-8)
int positive = -3 * -3;   // Negative times negative = positive (9)
```

# Visualization

```mermaid
flowchart TD
    A([The Multiplication Operator in C#]) --> B[What is the * Operator?]
    A --> C[Basic Usage]
    A --> D[Multiplication vs Addition]
    A --> E[Special Cases]

    B --> B1[Multiplies two numbers together]
    B1 --> B2[Used for products, areas, and scaling values]

    C --> C1[Example: 5 * 3 = 15]
    C --> C2[Example: 7 * 2 = 14]
    C --> C3[Example: 100 * 10 = 1000]

    D --> D1[Addition - combines values one by one]
    D --> D2[Multiplication - repeats a value a set number of times]
    D1 --> D1a[Example: 4 + 4 + 4 = 12]
    D2 --> D2a[Example: 4 * 3 = 12 - shorter and cleaner]
    D1a --> D3[Both produce the same result]
    D2a --> D3

    E --> E1[Any number times zero]
    E --> E2[Any number times one]
    E --> E3[Positive times negative]
    E --> E4[Negative times negative]
    E1 --> E1a[Result is always 0 - Example: 5 * 0 = 0]
    E2 --> E2a[Result is itself - Example: 8 * 1 = 8]
    E3 --> E3a[Result is negative - Example: 4 * -2 = -8]
    E4 --> E4a[Result is positive - Example: -3 * -3 = 9]
```

The flowchart branches into four sections. **What is the \* Operator?** establishes the definition and use cases, **Basic Usage** shows three straightforward examples, **Multiplication vs Addition** contrasts the two operators converging on the same result, and **Special Cases** maps the four key rules around zero, one, and sign combinations.
