# String Interpolation

String interpolation lets you embed variables and expressions directly inside strings using the `$` prefix and curly braces `{}`.

## Basic Syntax

```cs
string name = "Alice";
int score = 95;

// Without interpolation (concatenation)
string message1 = "Hello, " + name + "! Your score is " + score + ".";

// With interpolation (cleaner!)
string message2 = $"Hello, {name}! Your score is {score}.";
```

## Embedding Different Types

```cs
int quantity = 3;
double price = 9.99;
decimal total = 29.97m;

Console.WriteLine($"You bought {quantity} items");
Console.WriteLine($"Price per item: ${price}");
Console.WriteLine($"Total: ${total}");
```

## Expressions Inside Braces

You can put any C# expression inside the curly braces:

```cs
int a = 5;
int b = 3;
Console.WriteLine($"Sum: {a + b}");  // Prints: Sum: 8
Console.WriteLine($"Product: {a * b}");  // Prints: Product: 15
```

# Visualization

```mermaid
flowchart TD
    A([String Interpolation in C#]) --> B[What is String Interpolation?]
    A --> C[Basic Syntax]
    A --> D[Embedding Different Types]
    A --> E[Expressions Inside Braces]

    B --> B1[Embed variables and expressions directly inside strings]
    B1 --> B2[Uses the $ prefix before the opening quote]
    B2 --> B3[Variables and expressions wrapped in curly braces]
    B3 --> B4[Cleaner and more readable than concatenation]

    C --> C1[Without interpolation - concatenation]
    C --> C2[With interpolation]
    C1 --> C1a[Hello + name + Your score is + score]
    C1a --> C1b[Cluttered with + operators and quotes]
    C2 --> C2a[$ prefix added before opening quote]
    C2a --> C2b[Variables placed inside curly braces]
    C2b --> C2c[Example: Hello, name! Your score is score]
    C2c --> C2d[Result: Hello, Alice! Your score is 95]

    D --> D1[int - Example: quantity = 3]
    D --> D2[double - Example: price = 9.99]
    D --> D3[decimal - Example: total = 29.97m]
    D1 --> D1a[You bought 3 items]
    D2 --> D2a[Price per item: $9.99]
    D3 --> D3a[Total: $29.97]

    E --> E1[Any valid C# expression can go inside curly braces]
    E1 --> E2[Addition example: a + b inside braces]
    E2 --> E2a[Sum: 8]
    E1 --> E3[Multiplication example: a * b inside braces]
    E3 --> E3a[Product: 15]
```
