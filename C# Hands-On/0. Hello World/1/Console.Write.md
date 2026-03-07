# Console.Write vs Console.WriteLine

In C#, you have two main ways to output text: `Console.WriteLine()` adds a newline after the text, while `Console.Write()` keeps the cursor on the same line.

```cs
// Console.WriteLine adds a newline after output
Console.WriteLine("Hello");
Console.WriteLine("World");
// Output:
// Hello
// World

// Console.Write stays on the same line
Console.Write("Hello");
Console.Write("World");
// Output: HelloWorld
```

## Combining Both Methods

```cs
// You can mix Write and WriteLine
Console.Write("Name: ");
Console.WriteLine("Alice");
// Output: Name: Alice

Console.Write("Score: ");
Console.Write(100);
Console.WriteLine(" points");
// Output: Score: 100 points
```

## Key Differences

| Method                | Adds Newline | Use Case                       |
| --------------------- | ------------ | ------------------------------ |
| `Console.WriteLine()` | Yes          | Complete lines of output       |
| `Console.Write()`     | No           | Building output piece by piece |

## Visualization:

```mermaid
flowchart TD
    A([Console.Write vs Console.WriteLine]) --> B[Console.WriteLine]
    A --> C[Console.Write]
    A --> D[Combining Both Methods]
    A --> E[Key Differences]

    B --> B1[Adds a newline after the text]
    B1 --> B2[Cursor moves to the next line]
    B2 --> B3[Each call appears on its own line]
    B3 --> B4[Example: Console.WriteLine - Hello then Console.WriteLine - World]
    B4 --> B5[Output: Hello on line 1, World on line 2]

    C --> C1[Keeps cursor on the same line]
    C1 --> C2[No newline added after text]
    C2 --> C3[Multiple calls appear joined together]
    C3 --> C4[Example: Console.Write - Hello then Console.Write - World]
    C4 --> C5[Output: HelloWorld on one line]

    D --> D1[Write and WriteLine can be mixed freely]
    D1 --> D2[Example: Console.Write - Name: then Console.WriteLine - Alice]
    D2 --> D3[Output: Name: Alice on one line]
    D3 --> D4[Write builds partial output, WriteLine completes the line]

    E --> E1[Console.WriteLine]
    E --> E2[Console.Write]
    E1 --> E1a[Adds newline - Yes]
    E1 --> E1b[Use case: Complete lines of output]
    E2 --> E2a[Adds newline - No]
    E2 --> E2b[Use case: Building output piece by piece]
```
