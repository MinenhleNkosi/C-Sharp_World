# Logical AND Operator (&&)

The logical AND operator (`&&`) combines two boolean conditions and returns `true` only when both conditions are true.

## Basic Usage

```cs
bool result1 = true && true;   // True - both are true
bool result2 = true && false;  // False - second is false
bool result3 = false && true;  // False - first is false
bool result4 = false && false; // False - both are false
```

## Combining Comparison Operators

The `&&` operator is often used with comparison operators to check multiple conditions:

```cs
int age = 25;
bool hasLicense = true;

// Both conditions must be true
bool canDrive = age >= 18 && hasLicense;  // True

int temperature = 72;
bool isComfortable = temperature >= 65 && temperature <= 80;  // True
```

## Short-Circuit Evaluation

C# uses short-circuit evaluation: if the first condition is `false`, the second condition is not evaluated (since the result must be `false`):

```cs
bool a = false && SomeExpensiveMethod();  // SomeExpensiveMethod() never runs
```

## Truth Table

| Condition A | Condition B | A && B |
| ----------- | ----------- | ------ |
| True        | True        | True   |
| True        | False       | False  |
| False       | True        | False  |
| False       | False       | False  |

|

# Visualization

```mermaid
flowchart TD
    A([Logical AND Operator in C#]) --> B[What is the && Operator?]
    A --> C[Basic Usage]
    A --> D[Combining Comparison Operators]
    A --> E[Short-Circuit Evaluation]
    A --> F[Truth Table]

    B --> B1[Combines two boolean conditions]
    B1 --> B2[Returns true ONLY when both conditions are true]
    B2 --> B3[Returns false if either or both conditions are false]

    C --> C1[true && true = true - both are true]
    C --> C2[true && false = false - second is false]
    C --> C3[false && true = false - first is false]
    C --> C4[false && false = false - both are false]

    D --> D1[Often used with comparison operators]
    D1 --> D2[Check multiple conditions at once]
    D2 --> D3[Example: age and license check]
    D2 --> D4[Example: temperature range check]
    D3 --> D3a[age >= 18 AND hasLicense = true]
    D3a --> D3b[Both must be true to canDrive]
    D4 --> D4a[temperature >= 65 AND temperature <= 80]
    D4a --> D4b[Both must be true to isComfortable]

    E --> E1[If first condition is false - second is not evaluated]
    E1 --> E2[Result must already be false so second check is skipped]
    E2 --> E3[Example: false AND SomeExpensiveMethod]
    E3 --> E4[SomeExpensiveMethod never runs - saves processing time]

    F --> F1[True AND True = True]
    F --> F2[True AND False = False]
    F --> F3[False AND True = False]
    F --> F4[False AND False = False]
    F1 --> F5[Only this combination returns true]
    F2 --> F6[Any false condition makes result false]
    F3 --> F6
    F4 --> F6
```

The flowchart branches into five sections. **What is the && Operator?** establishes the core rule, **Basic Usage** maps all four boolean combinations and their results, **Combining Comparison Operators** shows two real-world examples of chaining conditions, **Short-Circuit Evaluation** explains the performance optimisation of skipping the second condition, and **Truth Table** summarises all combinations converging on the key insight that only one combination returns true.
