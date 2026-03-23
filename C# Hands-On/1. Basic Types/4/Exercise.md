# Your Task

Print a formatted message with exactly 4 lines:

- `"Welcome to C#!"` (with the quote marks visible)
- An empty line
- `Path: C:\Users\Documents` (with single backslashes)
- `Indented with a tab` (starting with a tab character)

## Method Signature

```cs
public static void PrintFormattedMessage()
```

## Expected Output

```cs
"Welcome to C#!"

Path: C:\Users\Documents
	Indented with a tab
```

## Hints

💡 1. Use `\"` to include quote marks inside your string - the backslash tells C# to treat the quote as text, not as the end of the string

💡 2. Use `\\` for each backslash you want to display - one backslash escapes the other

💡 3. Use `\`t at the start of a string to begin with a tab character

💡 4. An empty `Console.WriteLine()` or `Console.WriteLine("")` prints an empty line
