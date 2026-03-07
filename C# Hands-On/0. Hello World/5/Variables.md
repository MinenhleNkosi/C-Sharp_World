# Variables in C#

Variables are containers that store data values. You declare a variable by specifying its type and giving it a name.

## Declaring Variables

```cs
// Syntax: type variableName = value;
int age = 25;
bool isActive = true;
double price = 9.99;
```

## Common Data Types

```cs
// Syntax: type variableName = value;
int age = 25;
bool isActive = true;
double price = 9.99;
```

## Common Data Types

| Type     | Description     | Example   |
| -------- | --------------- | --------- |
| `int`    | Whole numbers   | `42`      |
| `double` | Decimal numbers | `3.14`    |
| `bool`   | True or false   | `true`    |
| `string` | Text/characters | `"Hello"` |

## Variable Naming Rules

```cs
// Valid variable names
int playerScore = 100;
bool isGameOver = false;
int totalItems = 5;

// Invalid - cannot start with number
// int 1stPlace = 1;  // Error!

// Invalid - cannot use reserved words
// int class = 5;  // Error!
```

## Basic Math Operations

You can perform calculations with numbers:

```cs
int a = 10;
int b = 3;

int sum = a + b;       // 13
int difference = a - b; // 7
int product = a * b;    // 30
int quotient = a / b;   // 3 (integer division)
```

## What is a Method?

A **method** is a reusable block of code that performs a specific task. Think of it like a recipe - you give it ingredients (inputs), it follows instructions, and gives you a result (output).

```cs
// This is a method that takes a number and returns its double
public static int DoubleNumber(int number)
{
    // The code inside the { } is what the method does
    int result = number * 2;
    return result;  // This sends the result back
}
```

**Breaking down the method signature**:

- `public static` - Don't worry about these for now, they're required keywords
- `int` - The **return type** - what kind of value this method gives back
- `DoubleNumber` - The **name** of the method
- `(int number)` - The **parameter** - input the method receives

## The `return` Keyword

The `return` keyword sends a value back from a method. Think of it like giving an answer to a question:

```cs
// Someone asks: "What's double of 5?"
// The method answers: 10

public static int DoubleNumber(int number)
{
    int doubled = number * 2;
    return doubled;  // This is the answer!
}
```

When a method has a return type (like `int`), it must use `return` to send back a value of that type.

## Visualization

```mermaid
flowchart TD
    A([Variables in C#]) --> B[Declaring Variables]
    A --> C[Common Data Types]
    A --> D[Variable Naming Rules]
    A --> E[Basic Math Operations]
    A --> F[What is a Method?]
    A --> G[The Return Keyword]

    B --> B1[Syntax: type variableName = value]
    B1 --> B2[Example: int age = 25]
    B1 --> B3[Example: bool isActive = true]
    B1 --> B4[Example: double price = 9.99]

    C --> C1[int - Whole numbers - Example: 42]
    C --> C2[double - Decimal numbers - Example: 3.14]
    C --> C3[bool - True or false - Example: true]
    C --> C4[string - Text and characters - Example: Hello]

    D --> D1[Valid names]
    D --> D2[Invalid names]
    D1 --> D1a[playerScore]
    D1 --> D1b[isGameOver]
    D1 --> D1c[totalItems]
    D2 --> D2a[Cannot start with a number - 1stPlace is invalid]
    D2 --> D2b[Cannot use reserved words - class is invalid]

    E --> E1[Addition: a + b = 13]
    E --> E2[Subtraction: a - b = 7]
    E --> E3[Multiplication: a * b = 30]
    E --> E4[Division: a / b = 3 - integer division]

    F --> F1[A reusable block of code that performs a task]
    F1 --> F2[Method Signature breakdown]
    F2 --> F2a[public static - required keywords]
    F2 --> F2b[int - the return type]
    F2 --> F2c[DoubleNumber - the method name]
    F2 --> F2d[int number - the parameter]
    F1 --> F3[Code inside curly braces is what the method does]

    G --> G1[Sends a value back from a method]
    G1 --> G2[Method must return a value matching its return type]
    G2 --> G3{Return type matches declared type?}
    G3 --> |Yes| G4[Valid - example: return doubled inside int method]
    G3 --> |No| G5[Invalid - compiler error]
```
