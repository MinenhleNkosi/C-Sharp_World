# The Modulo Operator

The modulo operator (`%`) returns the remainder after integer division. It's essential for tasks like checking even/odd numbers, cycling through values, and wrapping indices.

## Basic Usage

```cs
int remainder = 17 % 5;  // 2 (because 17 = 5 * 3 + 2)
int noRemainder = 10 % 2; // 0 (10 divides evenly by 2)
int smallerDividend = 3 % 7; // 3 (3 is less than 7, so remainder is 3)
```

## Division vs Modulo

```cs
// Division gives you how many times divisor fits
int quotient = 17 / 5;   // 3

// Modulo gives you what's left over
int remainder = 17 % 5;  // 2

// Together they satisfy: dividend = (quotient * divisor) + remainder
// 17 = (3 * 5) + 2 ✓
```

## Common Use Cases

| Pattern        | Example               | Result               |
| -------------- | --------------------- | -------------------- |
| Check if even  | `number % 2 == 0`     | true if even         |
| Check if odd   | `number % 2 != 0`     | true if odd          |
| Get last digit | `number % 10`         | ones place           |
| Wrap around    | `index % arrayLength` | cycles 0 to length-1 |

# Visualization

```mermaid
flowchart TD
    A([The Modulo Operator in C#]) --> B[What is the % Operator?]
    A --> C[Basic Usage]
    A --> D[Division vs Modulo]
    A --> E[Common Use Cases]

    B --> B1[Returns the remainder after integer division]
    B1 --> B2[Essential for checking even and odd numbers]
    B1 --> B3[Useful for cycling through values and wrapping indices]

    C --> C1[Example: 17 % 5 = 2 because 17 = 5 * 3 + 2]
    C --> C2[Example: 10 % 2 = 0 because 10 divides evenly]
    C --> C3[Example: 3 % 7 = 3 because 3 is smaller than 7]

    D --> D1[Division - how many times divisor fits]
    D --> D2[Modulo - what is left over]
    D1 --> D1a[Example: 17 / 5 = 3]
    D2 --> D2a[Example: 17 % 5 = 2]
    D1a --> D3[Together: dividend = quotient * divisor + remainder]
    D2a --> D3
    D3 --> D3a[Proof: 17 = 3 * 5 + 2]

    E --> E1[Check if even]
    E --> E2[Check if odd]
    E --> E3[Get last digit]
    E --> E4[Wrap around]
    E1 --> E1a[number % 2 == 0 returns true if even]
    E2 --> E2a[number % 2 != 0 returns true if odd]
    E3 --> E3a[number % 10 returns the ones place digit]
    E4 --> E4a[index % arrayLength cycles from 0 to length - 1]
```

The flowchart branches into four sections. **What is the % Operator?** establishes the definition and key use cases, **Basic Usage** covers the three core scenarios including when the dividend is smaller than the divisor, **Division vs Modulo** contrasts the two operators and shows how they relate through the remainder formula, and **Common Use Cases** maps each pattern to its example and result.
