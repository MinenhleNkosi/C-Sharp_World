# Division Operator

The division operator `/` divides one number by another. Unlike integer division, using `double` preserves decimal precision.

## Basic Usage

```cs
double result1 = 10.0 / 2.0;  // result1 = 5.0
double result2 = 7.0 / 2.0;   // result2 = 3.5
double result3 = 1.0 / 4.0;   // result3 = 0.25
```

## Integer vs Double Division

When dividing integers, C# truncates the decimal portion. Using `double` preserves it.

```cs
int intResult = 7 / 2;        // intResult = 3 (truncated!)
double doubleResult = 7.0 / 2.0;  // doubleResult = 3.5 (preserved)
```

## Special Cases

```cs
double divByZero = 5.0 / 0.0;     // Result: Infinity
double zeroNumerator = 0.0 / 5.0; // Result: 0
double negResult = -10.0 / 4.0;   // Result: -2.5
```

# Visualization

```mermaid
flowchart TD
    A([The Division Operator in C#]) --> B[What is the / Operator?]
    A --> C[Basic Usage]
    A --> D[Integer vs Double Division]
    A --> E[Special Cases]

    B --> B1[Divides one number by another]
    B1 --> B2[Using double preserves decimal precision]
    B2 --> B3[Using int truncates the decimal portion]

    C --> C1[Example: 10.0 / 2.0 = 5.0]
    C --> C2[Example: 7.0 / 2.0 = 3.5]
    C --> C3[Example: 1.0 / 4.0 = 0.25]

    D --> D1[Integer division]
    D --> D2[Double division]
    D1 --> D1a[Decimal portion is truncated - cut off]
    D1 --> D1b[Example: 7 / 2 = 3 - not 3.5]
    D2 --> D2a[Decimal portion is preserved]
    D2 --> D2b[Example: 7.0 / 2.0 = 3.5]
    D1b --> D3{Need decimal precision?}
    D2b --> D3
    D3 --> |Yes| D4[Use double]
    D3 --> |No| D5[int is fine]

    E --> E1[Divide by zero]
    E --> E2[Zero as numerator]
    E --> E3[Negative division]
    E1 --> E1a[Example: 5.0 / 0.0 = Infinity]
    E2 --> E2a[Example: 0.0 / 5.0 = 0]
    E3 --> E3a[Example: -10.0 / 4.0 = -2.5]
```

The flowchart branches into four sections. **What is the / Operator?** establishes the definition and the key distinction between int and double behaviour, **Basic Usage** shows three double division examples, **Integer vs Double Division** contrasts the two with a decision point on whether decimal precision is needed, and **Special Cases** maps the three edge case scenarios and their results.
