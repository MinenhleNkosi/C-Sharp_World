# Console.ReadLine

`Console.ReadLine()` reads a line of text that the user types and returns it as a string. It waits for the user to press Enter, then gives you everything they typed.

```cs
string input = Console.ReadLine();
Console.WriteLine(input);
```

The program pauses at `Console.ReadLine()` until the user types something and presses Enter. Whatever they typed gets stored in the variable.

## Storing Input in Variables

```cs
// Read and store in a variable
string name = Console.ReadLine();

// Now you can use the variable
Console.WriteLine(name);
```

## Visualization

```mermaid
flowchart TD
    A([Console.ReadLine]) --> B[How It Works]
    A --> C[Storing Input in Variables]

    B --> B1[Waits for the user to type input]
    B1 --> B2[Program pauses until Enter is pressed]
    B2 --> B3[Returns everything typed as a string]
    B3 --> B4[Example: string input = Console.ReadLine]
    B4 --> B5[Pass input to Console.WriteLine to display it]

    C --> C1[Store returned string in a named variable]
    C1 --> C2[Example: string name = Console.ReadLine]
    C2 --> C3{User presses Enter}
    C3 --> |Input received| C4[Value stored in the variable]
    C3 --> |Nothing typed| C5[Empty string stored in the variable]
    C4 --> C6[Variable can now be used anywhere in the program]
    C5 --> C6
```
