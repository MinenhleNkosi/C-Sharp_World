# Compound Assignment Operators

Compound assignment operators combine an arithmetic operation with assignment, making code more concise when you want to modify a variable's value based on itself.

## Standard vs Compound Assignment

```cs
// Standard assignment - verbose
int score = 10;
score = score + 5;  // score is now 15

// Compound assignment - concise
int score = 10;
score += 5;  // score is now 15 (same result!)
```

## The Four Arithmetic Compound Operators

```cs
int x = 20;

x += 5;   // x = x + 5  → x is now 25
x -= 3;   // x = x - 3  → x is now 22
x *= 2;   // x = x * 2  → x is now 44
x /= 4;   // x = x / 4  → x is now 11
```

## Quick Reference

| Operator | Meaning             | Example  | Result (if x = 10) |
| -------- | ------------------- | -------- | ------------------ |
| `+=`     | Add and assign      | `x += 3` | x becomes 13       |
| `-=`     | Subtract and assign | `x -= 3` | x becomes 7        |
| `*=`     | Multiply and assign | `x *= 3` | x becomes 30       |
| `/=`     | Divide and assign   | `x /= 2` | x becomes 5        |

# Visualization

```mermaid
flowchart TD
    A([Compound Assignment Operators in C#]) --> B[What Are Compound Assignment Operators?]
    A --> C[Standard vs Compound Assignment]
    A --> D[The Four Arithmetic Compound Operators]
    A --> E[Quick Reference]

    B --> B1[Combine an arithmetic operation with assignment]
    B1 --> B2[Modify a variable's value based on itself]
    B2 --> B3[Makes code more concise and readable]

    C --> C1[Standard assignment - verbose]
    C --> C2[Compound assignment - concise]
    C1 --> C1a[score = score + 5]
    C1a --> C1b[score is now 15]
    C2 --> C2a[score += 5]
    C2a --> C2b[score is now 15 - same result]
    C1b --> C3[Both produce identical results]
    C2b --> C3

    D --> D1[Start: int x = 20]
    D1 --> D2[x += 5 - x = x + 5 - x is now 25]
    D2 --> D3[x -= 3 - x = x - 3 - x is now 22]
    D3 --> D4[x *= 2 - x = x * 2 - x is now 44]
    D4 --> D5[x /= 4 - x = x / 4 - x is now 11]

    E --> E1[+= Add and assign]
    E --> E2[-= Subtract and assign]
    E --> E3[*= Multiply and assign]
    E --> E4[/= Divide and assign/]
    E1 --> E1a[x += 3 where x = 10 - x becomes 13]
    E2 --> E2a[x -= 3 where x = 10 - x becomes 7]
    E3 --> E3a[x *= 3 where x = 10 - x becomes 30]
    E4 --> E4a[x /= 2 where x = 10 - x becomes 5]
```

The flowchart branches into four sections. **What Are Compound Assignment Operators?** establishes the concept, **Standard vs Compound Assignment** contrasts the two approaches converging on the same result, **The Four Arithmetic Compound Operators** traces a sequential chain showing how x changes with each operation, and **Quick Reference** maps each operator to its meaning and result when starting from x = 10.
