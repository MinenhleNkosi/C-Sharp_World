# Escape Sequences

Escape sequences are special character combinations that represent characters which cannot be typed directly in a string, like _newlines_, _tabs_, or _quote marks_.

## Common Escape Sequences

| Sequence | Description  | Example Output |
| -------- | ------------ | -------------- |
| `\n`     | New line     | Line 1↵Line 2  |
| `\t`     | Tab (indent) | Hello→World    |
| `\\`     | Backslash    | C:\Users       |
| `\"`     | Double quote | He said "Hi"   |

## Using Escape Sequences

```cs
// Newline - creates multiple lines
Console.WriteLine("Line 1\nLine 2");
// Output:
// Line 1
// Line 2

// Tab - adds horizontal spacing
Console.WriteLine("Name:\tJohn");
// Output: Name: John

// Backslash - for file paths
Console.WriteLine("C:\\Program Files\\App");
// Output: C:\Program Files\App

// Quotes inside strings
Console.WriteLine("She said \"Hello!\"");
// Output: She said "Hello!"
```

## Combining Escape Sequences

```cs
Console.WriteLine("\"Quote\"\n\tIndented line");
// Output:
// "Quote"
// Indented line
```

# Visualization

```mermaid
flowchart TD
    A([Escape Sequences in C#]) --> B[What Are Escape Sequences?]
    A --> C[Common Escape Sequences]
    A --> D[Using Escape Sequences]
    A --> E[Combining Escape Sequences]

    B --> B1[Special character combinations]
    B1 --> B2[Represent characters that cannot be typed directly in a string]
    B2 --> B3[Always start with a backslash]

    C --> C1[backslash-n - New line]
    C --> C2[backslash-t - Tab indent]
    C --> C3[backslash-backslash - Backslash]
    C --> C4[backslash-quote - Double quote]
    C1 --> C1a[Output: Line 1 then Line 2 on next line]
    C2 --> C2a[Output: Hello then horizontal space then World]
    C3 --> C3a[Output: C:\Users]
    C4 --> C4a[Output: He said "Hi"]

    D --> D1[Newline example]
    D --> D2[Tab example]
    D --> D3[Backslash example]
    D --> D4[Quotes example]
    D1 --> D1a[Console.WriteLine - Line 1\nLine 2]
    D1a --> D1b[Prints Line 1 and Line 2 on separate lines]
    D2 --> D2a[Console.WriteLine - Name:\tJohn]
    D2a --> D2b[Prints Name: then tabbed space then John]
    D3 --
```
