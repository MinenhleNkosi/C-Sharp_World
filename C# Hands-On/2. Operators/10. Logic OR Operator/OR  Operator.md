# Logical OR Operator

The logical OR operator (`||`) returns `true` if **at least one** of its operands is true. It's used when you need to check if any condition among several is satisfied.

## Basic Usage

```cs
bool result1 = true || false;   // true (first is true)
bool result2 = false || true;   // true (second is true)
bool result3 = false || false;  // false (neither is true)
bool result4 = true || true;    // true (both are true)
```

## OR vs AND

| Operator | Symbol | Returns true when...         |
| -------- | ------ | ---------------------------- |
| AND      | `&&`   | Both operands are true       |
| OR       | `\|\|` | At least one operand is true |

|

```cs
// AND - both must be true
bool canDrive = hasLicense && hasCar;  // needs BOTH

// OR - either can be true
bool canEnter = isAdult || hasParentConsent;  // needs at least ONE
```

## Short-Circuit Evaluation

The OR operator uses short-circuit evaluation: if the first operand is `true`, the second operand is **not evaluated** because the result is already known to be `true`.

```cs
bool result = true || SomeExpensiveCheck();  // SomeExpensiveCheck() never runs!
```

# Visualization

```mermaid
flowchart TD
    A([Logical OR Operator in C#]) --> B[What is the OR Operator?]
    A --> C[Basic Usage]
    A --> D[OR vs AND]
    A --> E[Short-Circuit Evaluation]

    B --> B1[Uses the double pipe symbol]
    B1 --> B2[Returns true if at least one operand is true]
    B2 --> B3[Returns false only when both operands are false]

    C --> C1[true OR false = true - first is true]
    C --> C2[false OR true = true - second is true]
    C --> C3[false OR false = false - neither is true]
    C --> C4[true OR true = true - both are true]
    C3 --> C5[Only this combination returns false]

    D --> D1[AND - both operands must be true]
    D --> D2[OR - at least one operand must be true]
    D1 --> D1a[Example: canDrive = hasLicense AND hasCar]
    D1a --> D1b[Needs BOTH conditions to be true]
    D2 --> D2a[Example: canEnter = isAdult OR hasParentConsent]
    D2a --> D2b[Needs at least ONE condition to be true]

    E --> E1[If first operand is true - second is not evaluated]
    E1 --> E2[Result is already known to be true]
    E2 --> E3[Example: true OR SomeExpensiveCheck]
    E3 --> E4[SomeExpensiveCheck never runs - saves processing time]
    E1 --> E5[Opposite of AND short-circuit]
    E5 --> E6[AND skips when first is false - OR skips when first is true]
```

The flowchart branches into four sections. **What is the OR Operator?** establishes the core rule, **Basic Usage** maps all four boolean combinations highlighting the only one that returns false, **OR vs AND** contrasts the two operators with real-world examples showing the difference between needing both vs needing one, and **Short-Circuit Evaluation** explains how OR skips the second operand when the first is already true, noting how this is the opposite of AND's short-circuit behaviour.
