# Single-Line Comments

Comments are notes in your code that the computer ignores. They help you and other programmers understand what the code does.

## Writing Comments

In C#, single-line comments start with `//`. Everything after `//` on that line is ignored.

```cs
// This is a comment - the computer ignores this
Console.WriteLine("Hello"); // You can also comment at the end of a line
```

## Why Use Comments?

- **Explain your code**: Describe what complex logic does
- **Leave notes**: Remind yourself why you wrote something
- **Disable code**: Temporarily stop code from running without deleting it

```cs
// Calculate the area of a circle
double area = 3.14 * radius * radius;

// Console.WriteLine("Debug message"); // This line won't run
```

## Commenting Out Code

You can "comment out" code to disable it temporarily:

```cs
Console.WriteLine("This prints");
// Console.WriteLine("This does NOT print");
```

## Visualization

```mermaid
flowchart TD
    A([Single-Line Comments in C#]) --> B[What Are Comments?]
    A --> C[Writing Comments]
    A --> D[Why Use Comments?]
    A --> E[Commenting Out Code]

    B --> B1[Notes in your code]
    B1 --> B2[The computer completely ignores them]
    B2 --> B3[Help you and others understand the code]

    C --> C1[Start with double forward slash - //]
    C1 --> C2[Everything after // on that line is ignored]
    C2 --> C3[Can appear on its own line]
    C2 --> C4[Can appear at the end of a line of code]
    C3 --> C5[Example: // This is a comment]
    C4 --> C6[Example: Console.WriteLine - Hello - // inline comment]

    D --> D1[Explain your code]
    D --> D2[Leave notes for yourself]
    D --> D3[Disable code temporarily]
    D1 --> D1a[Describe what complex logic does]
    D2 --> D2a[Remind yourself why you wrote something]
    D3 --> D3a[Stop code from running without deleting it]

    E --> E1[Add // before any line of code]
    E1 --> E2{Does the line start with //?}
    E2 --> |Yes| E3[Line is ignored - does not execute]
    E2 --> |No| E4[Line runs normally]
    E3 --> E5[Example: // Console.WriteLine - This does NOT print]
    E4 --> E6[Example: Console.WriteLine - This prints]
```
