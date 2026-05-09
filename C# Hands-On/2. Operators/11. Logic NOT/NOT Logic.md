# Logical NOT Operator

The logical NOT operator (`!`) inverts a boolean value. If a value is `true`, it becomes `false`, and vice versa.

## Basic Usage

```cs
bool isOpen = true;
bool isClosed = !isOpen;  // false

bool hasError = false;
bool isValid = !hasError; // true
```

## Common Use Cases

The NOT operator is frequently used to:

- Check if something is NOT true
- Toggle boolean states
- Simplify negative conditions

```cs
// Instead of checking == false
if (isLoggedIn == false) { }  // Works but verbose

// Use the NOT operator
if (!isLoggedIn) { }          // Cleaner and preferred

// Double negation returns original value
bool active = true;
bool result = !!active;  // true (negated twice)
```

## Combining with Other Operators

```cs
bool a = true;
bool b = false;

bool result1 = !a && b;   // false && false = false
bool result2 = !(a && b); // !(true && false) = !false = true
bool result3 = !a || !b;  // false || true = true
```

# Visualization

```mermaid
flowchart TD
    A([Logical NOT Operator in C#]) --> B[What is the NOT Operator?]
    A --> C[Basic Usage]
    A --> D[Common Use Cases]
    A --> E[Combining with Other Operators]

    B --> B1[Uses the exclamation mark symbol - !]
    B1 --> B2[Inverts a boolean value]
    B2 --> B3[true becomes false]
    B2 --> B4[false becomes true]

    C --> C1[Example: isOpen = true]
    C1 --> C1a[!isOpen = false - stored as isClosed]
    C --> C2[Example: hasError = false]
    C2 --> C2a[!hasError = true - stored as isValid]

    D --> D1[Check if something is NOT true]
    D --> D2[Toggle boolean states]
    D --> D3[Simplify negative conditions]
    D1 --> D1a[Verbose: if isLoggedIn == false]
    D1 --> D1b[Preferred: if !isLoggedIn - cleaner]
    D --> D4[Double negation returns original value]
    D4 --> D4a[!!active where active = true]
    D4a --> D4b[First ! makes it false]
    D4b --> D4c[Second ! makes it true again]

    E --> E1[!a AND b]
    E --> E2[NOT of a AND b]
    E --> E3[!a OR !b]
    E1 --> E1a[!true AND false = false AND false = false]
    E2 --> E2a[NOT of true AND false = NOT false = true]
    E3 --> E3a[!true OR !false = false OR true = true]
    E2 --> E2b[Parentheses change the result vs E1]
    E1 --> E2b
```

The flowchart branches into four sections. **What is the NOT Operator?** establishes the inversion rule for both directions, **Basic Usage** traces two concrete examples showing the value flip, **Common Use Cases** covers the three main scenarios including the double negation behaviour, and **Combining with Other Operators** shows how placement of the NOT operator changes results, highlighting the key difference between `!a && b` and `!(a && b)`.
