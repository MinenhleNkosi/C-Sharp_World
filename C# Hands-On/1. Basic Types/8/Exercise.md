# Your Task

Write a method that takes a character and prints four lines of information about it:

- The character itself
- Whether it's a letter (`True` or `False`)
- Whether it's a digit (`True` or `False`)
- Whether it's uppercase (`True` or `False`)

## Method Signature

```cs
public static void PrintCharInfo(char c)
```

## Expected Output

```cs
PrintCharInfo('A') prints:
A
True
False
True

PrintCharInfo('7') prints:
7
False
True
False
```

## Hints

💡 1. Use `Console.WriteLine()` four times, once for each piece of information.

💡 2. The `char` class has static methods like `char.IsLetter(c)` that return `bool`.

💡 3. Remember that `char.IsUpper()` returns `False` for non-letters like digits and symbols.
