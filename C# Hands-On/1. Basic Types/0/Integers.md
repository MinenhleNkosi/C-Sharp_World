# The int Type

The `int` type stores whole numbers (integers) - both positive and negative values, but no decimals. It is a **32-bit signed integer**, meaning it uses 32 bits (4 bytes) of memory to store values.

## Declaring int Variables

```cs
// Declare and assign in one line
int age = 25;
int year = 2024;

// Declare first, assign later
int score;
score = 100;
```

## Positive and Negative Numbers

```cs
int temperature = -10; // Negative number
int altitude = 8848; // Positive number
int balance = 0; // Zero is valid too
```

## Basic Math with int

```cs
int a = 10;
int b = 3;
int sum = a + b; // 13
int difference = a - b; // 7
int product = a \* b; // 30
```

## int Range (32-bit)

Because `int` is a 32-bit signed integer, it can store values in this range:

| Property  | Value             |
| --------- | ----------------- |
| Size      | 32 bits (4 bytes) |
| Min Value | -2,147,483,648    |
| Max Value | 2,147,483,647     |

You can access these limits in code using `int.MinValue` and `int.MaxValue`.

# Visualization

```mermaid
flowchart TD
    A([The int Type]) --> B[What is int?]
    A --> C[Declaring int Variables]
    A --> D[Positive and Negative Numbers]
    A --> E[Basic Math with int]
    A --> F[int Range - 32-bit]

    B --> B1[Stores whole numbers - no decimals]
    B1 --> B2[Both positive and negative values]
    B2 --> B3[32-bit signed integer]
    B3 --> B4[Uses 32 bits - 4 bytes - of memory]

    C --> C1[Declare and assign in one line]
    C --> C2[Declare first, assign later]
    C1 --> C1a[Example: int age = 25]
    C1 --> C1b[Example: int year = 2024]
    C2 --> C2a[Example: int score - then score = 100]

    D --> D1[Positive numbers - Example: int altitude = 8848]
    D --> D2[Negative numbers - Example: int temperature = -10]
    D --> D3[Zero is valid - Example: int balance = 0]

    E --> E1[Addition: a + b = 13]
    E --> E2[Subtraction: a - b = 7]
    E --> E3[Multiplication: a * b = 30]

    F --> F1[Size: 32 bits - 4 bytes]
    F --> F2[Min Value: -2,147,483,648]
    F --> F3[Max Value: 2,147,483,647]
    F2 --> F4[Access in code: int.MinValue]
    F3 --> F5[Access in code: int.MaxValue]
```
