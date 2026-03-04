# Console.WriteLine

`Console.WriteLine()` is how you display text to the console in C#. Each call prints on a new line.

```cs
Console.WriteLine("Hello, World!");
// Output: Hello, World!

Console.WriteLine("First line");
Console.WriteLine("Second line");
// Output:
// First line
// Second line
```

## Variables and Strings

A **variable** is a named container that stores a value. Think of it like a labeled box where you can put something and retrieve it later by its name.

A **string** is a type of data that holds text - any sequence of characters like letters, numbers, or symbols surrounded by double quotes.

```cs
string name = "Alex";           // Creates a variable called 'name' that holds the text "Alex"
string favoriteColor = "Blue";  // Creates a variable called 'favoriteColor' that holds "Blue"
```

Breaking down the syntax:

- `string` - the data type (tells C# this variable will hold text)
- `name` - the variable name (you choose this - make it descriptive!)
- `=` - the assignment operator (puts the value into the variable)
- `"Alex"` - the value (the actual text, in double quotes)

## Printing Variables

You can print the value stored in a variable by passing the variable name (without quotes):

```cs
string greeting = "Welcome!";
Console.WriteLine(greeting);
// Output: Welcome!

string city = "London";
Console.WriteLine(city);
// Output: London
```

**Important**: When printing a variable, don't use quotes around the variable name:

```cs
Console.WriteLine(name);    // Prints the VALUE: Alex
Console.WriteLine("name");  // Prints the literal text: name
```

## WriteLine vs Write

| Method                | Description                            |
| --------------------- | -------------------------------------- |
| `Console.WriteLine()` | Prints text and moves to a new line    |
| `Console.Write()`     | Prints text but stays on the same line |

```cs
Console.Write("Hello ");
Console.Write("World");
// Output: Hello World (on one line)

Console.WriteLine("Hello");
Console.WriteLine("World");
// Output:
// Hello
// World
```

## Understanding the Code Structure

In C#, code is organized into **classes** and **methods**:

- **Class**: A container that groups related code together. In this exercise, `Solution` is the class name and `Solution.cs` is the file name. Think of it as a folder that holds your code.
- **Method**: A block of code that performs a specific task. `PrintNameAndColor` is the method name. Methods are like recipes - they contain the instructions to do something.

```cs
public class Solution           // This is the class
{
    public static void PrintNameAndColor()  // This is the method
    {
        // Code goes inside the method where you perform a specific task
    }
}
```

For now, just know that your code goes inside the method (between the curly braces `{ }`). You'll learn more about classes and methods later!

## Topic Visualization

```mermaid
flowchart TD
    A([Console.WriteLine]) --> B[Displaying Text]
    A --> C[Variables and Strings]
    A --> D[Printing Variables]
    A --> E[WriteLine vs Write]
    A --> F[Code Structure]

    B --> B1[Each call prints on a new line]
    B1 --> B2[Console.WriteLine - Hello World]
    B2 --> B3[Output appears on its own line]

    C --> C1[Variable: a named container that stores a value]
    C --> C2[String: a type that holds text in double quotes]
    C1 --> C3[Syntax breakdown]
    C3 --> C3a[string - the data type]
    C3 --> C3b[name - the variable name]
    C3 --> C3c[= - the assignment operator]
    C3 --> C3d[value - the actual text in double quotes]
    C2 --> C4[Example: string name = Alex]

    D --> D1[Pass variable name without quotes to print its value]
    D1 --> D2{Quotes around variable name?}
    D2 --> |No quotes - Console.WriteLine-name-| D3[Prints the VALUE: Alex]
    D2 --> |With quotes - Console.WriteLine-name-| D4[Prints literal text: name]

    E --> E1[Console.WriteLine]
    E --> E2[Console.Write]
    E1 --> E1a[Prints text and moves to a new line]
    E2 --> E2a[Prints text and stays on the same line]
    E1a --> E3[Multiple calls produce multiple lines]
    E2a --> E4[Multiple calls produce one continuous line]

    F --> F1[Class: a container that groups related code]
    F --> F2[Method: a block of code that performs a task]
    F1 --> F3[Example: public class Solution]
    F2 --> F4[Example: public static void PrintNameAndColor]
    F4 --> F5[Your code goes inside the method curly braces]
```
