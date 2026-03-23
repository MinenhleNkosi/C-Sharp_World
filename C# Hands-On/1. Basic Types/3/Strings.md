# Strings in C#

A string is a sequence of characters used to represent text. Strings are one of the most commonly used data types in programming.

## Declaring Strings

```cs
// Using the string keyword (preferred)
string name = "Alice";
string city = "New York";

// Strings can contain letters, numbers, spaces, and special characters
string message = "Order #12345 confirmed!";
```

## String vs Other Types

Unlike numeric types (`int`, `double`, `decimal`), strings hold text data enclosed in double quotes.

```cs
int age = 25;           // Number - no quotes
double price = 19.99;   // Number - no quotes
string name = "Bob";    // Text - requires double quotes
```

## Printing Strings

Use `Console.WriteLine()` to print a string to the console.

```cs
string greeting = "Hello!";
Console.WriteLine(greeting);  // Prints: Hello!

// You can also print string literals directly
Console.WriteLine("Goodbye!");  // Prints: Goodbye!
```

# Visualization

```memaid
flowchart TD
    A([Strings in C#]) --> B[What is a String?]
    A --> C[Declaring Strings]
    A --> D[String vs Other Types]
    A --> E[Printing Strings]

    B --> B1[A sequence of characters]
    B1 --> B2[Used to represent text]
    B2 --> B3[One of the most commonly used data types]

    C --> C1[Use the string keyword]
    C1 --> C2[Enclose value in double quotes]
    C2 --> C3[Example: string name = Alice]
    C2 --> C4[Example: string city = New York]
    C2 --> C5[Can contain letters, numbers, spaces, and special characters]
    C5 --> C6[Example: string message = Order 12345 confirmed!]

    D --> D1[Numeric types - int, double, decimal]
    D --> D2[String type]
    D1 --> D1a[Hold numeric data]
    D1 --> D1b[No quotes required]
    D1 --> D1c[Example: int age = 25]
    D1 --> D1d[Example: double price = 19.99]
    D2 --> D2a[Holds text data]
    D2 --> D2b[Requires double quotes]
    D2 --> D2c[Example: string name = Bob]

    E --> E1[Use Console.WriteLine to print a string]
    E1 --> E2{What are you printing?}
    E2 --> |A variable| E3[Pass variable name without quotes]
    E2 --> |A string literal| E4[Pass text directly in double quotes]
    E3 --> E3a[Example: Console.WriteLine-greeting- prints Hello!]
    E4 --> E4a[Example: Console.WriteLine-Goodbye!- prints Goodbye!]
```
