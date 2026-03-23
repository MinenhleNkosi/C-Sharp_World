# String Concatenation

String concatenation is the process of joining two or more strings together using the `+` operator. It's one of the most fundamental ways to build strings in C#.

## Basic String Concatenation

```cs
string greeting = "Hello" + " " + "World";
// Result: "Hello World"

string first = "John";
string last = "Doe";
string fullName = first + " " + last;
// Result: "John Doe"
```

## Concatenating Strings with Numbers

When you concatenate a string with a number, C# automatically converts the number to a string:

```cs
int score = 100;
string message = "Your score is: " + score;
// Result: "Your score is: 100"

double price = 19.99;
string priceTag = "Price: $" + price;
// Result: "Price: $19.99"
```

## Building Multi-Part Strings

```cs
string name = "Alice";
int age = 25;
string city = "London";

string bio = name + " is " + age + " years old and lives in " + city + ".";
// Result: "Alice is 25 years old and lives in London."
```

# Visualization

```mermaid
flowchart TD
    A([String Concatenation in C#]) --> B[What is String Concatenation?]
    A --> C[Basic String Concatenation]
    A --> D[Concatenating Strings with Numbers]
    A --> E[Building Multi-Part Strings]

    B --> B1[Joining two or more strings together]
    B1 --> B2[Uses the + operator]
    B2 --> B3[One of the most fundamental ways to build strings]

    C --> C1[Use + to join string values]
    C1 --> C2[Spaces must be added manually as separate strings]
    C2 --> C3[Example: Hello + space + World]
    C3 --> C4[Result: Hello World]
    C1 --> C5[Example: first + space + last]
    C5 --> C6[Result: John Doe]

    D --> D1[C# automatically converts numbers to strings]
    D1 --> D2[int example]
    D1 --> D3[double example]
    D2 --> D2a[Your score is: + score where score = 100]
    D2a --> D2b[Result: Your score is: 100]
    D3 --> D3a[Price: $ + price where price = 19.99]
    D3a --> D3b[Result: Price: $19.99]

    E --> E1[Multiple variables and strings joined with +]
    E1 --> E2[Mix of string and int variables]
    E2 --> E3[name + is + age + years old and lives in + city]
    E3 --> E4[Result: Alice is 25 years old and lives in London.]
```
